# ✅ GlassFish Base Image
FROM airhacks/glassfish

# ✅ Copy WAR into GlassFish autodeploy folder
COPY SilverRS.war /opt/glassfish4/glassfish/domains/domain1/autodeploy/

# ✅ Expose GlassFish Port
EXPOSE 8080

# ✅ Start GlassFish Server
CMD ["asadmin", "start-domain", "-v"]
