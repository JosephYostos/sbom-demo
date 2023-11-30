# sbom-demo

## Deploy Sock-Shop Application

 ```bash
kubectl apply -f https://raw.githubusercontent.com/JosephYostos/sbom-demo/main/sock-shop.yaml
 ```

## Install Sysdig cluster scanner on single cluster

https://sysdig-docs-pr-1444.onrender.com/en/docs/installation/sysdig-secure/install-agent-components/kubernetes/install-cluster-scanner/#full-deploy-with-cluster-scanner

## Extract SBOM


 ```bash
curl --request GET \
  -H "Authorization: Bearer xxx" \
  --url 'https://eu1.app.sysdig.com/secure/vulnerability/v1beta1/sboms?assetId=sha256:c276a3cc04187ca2e291256688a44a9b5db207762d14f21091b470f9c53794e2&assetType=container-image' | jq
 ```

## Output

 ```bash
{
  "$schema": "http://cyclonedx.org/schema/bom-1.5.schema.json",
  "bomFormat": "CycloneDX",
  "specVersion": "1.5",
  "serialNumber": "urn:uuid:656770b4-b9cf-4d88-809b-f86a33472801",
  "version": 1,
  "metadata": {
    "timestamp": "2023-11-29T17:11:17Z",
    "tools": [
      {
        "vendor": "sysdig",
        "name": "sysdig-image-sbom-extractor",
        "version": "v0.0.0-20231123152411-42f91b21a831"
      }
    ],
    "component": {
      "bom-ref": "243be7c9-ea6e-4a4f-823f-76a68478137b",
      "type": "container",
      "name": "sha256:c276a3cc04187ca2e291256688a44a9b5db207762d14f21091b470f9c53794e2"
    }
  },
  "components": [
    {
      "bom-ref": "77bf9328-4e89-4115-8a4c-1d0090a09bfd",
      "type": "operating-system",
      "name": "alpine",
      "version": "3.4.6"
    },
    {
      "bom-ref": "a2dc3112-96e1-4337-a359-33a053984083",
      "type": "library",
      "name": "musl",
      "version": "1.1.14-r16",
      "purl": "pkg:apk/alpine/musl@1.1.14-r16?distro=alpine-3.4.6&upstream=musl&upstream-version=1.1.14-r16",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:e53f74215d12318372e4412d0f0eb3908e17db25c6185f670db49aef5271f91f"
        },
        {
          "name": "sysdig:layer:index",
          "value": "0"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    },
    {
      "bom-ref": "ae74e6da-0c88-4c4c-8729-a92c81940fdb",
      "type": "library",
      "name": "busybox",
      "version": "1.24.2-r14",
      "purl": "pkg:apk/alpine/busybox@1.24.2-r14?distro=alpine-3.4.6&upstream=busybox&upstream-version=1.24.2-r14",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:e53f74215d12318372e4412d0f0eb3908e17db25c6185f670db49aef5271f91f"
        },
        {
          "name": "sysdig:layer:index",
          "value": "0"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    },
    {
      "bom-ref": "0ea44c44-94bb-48e5-bee3-870838b7da6f",
      "type": "library",
      "name": "alpine-baselayout",
      "version": "3.0.3-r0",
      "purl": "pkg:apk/alpine/alpine-baselayout@3.0.3-r0?distro=alpine-3.4.6&upstream=alpine-baselayout&upstream-version=3.0.3-r0",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:e53f74215d12318372e4412d0f0eb3908e17db25c6185f670db49aef5271f91f"
        },
        {
          "name": "sysdig:layer:index",
          "value": "0"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    },
    {
      "bom-ref": "3fdb8cc6-30d3-40ce-b0e9-d73b87275521",
      "type": "library",
      "name": "alpine-keys",
      "version": "1.1-r0",
      "purl": "pkg:apk/alpine/alpine-keys@1.1-r0?distro=alpine-3.4.6&upstream=alpine-keys&upstream-version=1.1-r0",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:e53f74215d12318372e4412d0f0eb3908e17db25c6185f670db49aef5271f91f"
        },
        {
          "name": "sysdig:layer:index",
          "value": "0"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    },
    {
      "bom-ref": "245c1287-36c6-4aa3-ba3b-d12185e8d952",
      "type": "library",
      "name": "zlib",
      "version": "1.2.11-r0",
      "purl": "pkg:apk/alpine/zlib@1.2.11-r0?distro=alpine-3.4.6&upstream=zlib&upstream-version=1.2.11-r0",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:e53f74215d12318372e4412d0f0eb3908e17db25c6185f670db49aef5271f91f"
        },
        {
          "name": "sysdig:layer:index",
          "value": "0"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    },
    {
      "bom-ref": "b3c5c9be-3500-43e6-acab-0ee273ee27d4",
      "type": "library",
      "name": "libcrypto1.0",
      "version": "1.0.2n-r0",
      "purl": "pkg:apk/alpine/libcrypto1.0@1.0.2n-r0?distro=alpine-3.4.6&upstream=openssl&upstream-version=1.0.2n-r0",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:e53f74215d12318372e4412d0f0eb3908e17db25c6185f670db49aef5271f91f"
        },
        {
          "name": "sysdig:layer:index",
          "value": "0"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    },
    {
      "bom-ref": "71962e9e-afba-4329-807c-e97a2037267e",
      "type": "library",
      "name": "libssl1.0",
      "version": "1.0.2n-r0",
      "purl": "pkg:apk/alpine/libssl1.0@1.0.2n-r0?distro=alpine-3.4.6&upstream=openssl&upstream-version=1.0.2n-r0",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:e53f74215d12318372e4412d0f0eb3908e17db25c6185f670db49aef5271f91f"
        },
        {
          "name": "sysdig:layer:index",
          "value": "0"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    },
    {
      "bom-ref": "dc7fa565-cb71-4403-8dc3-82676c6dde1e",
      "type": "library",
      "name": "apk-tools",
      "version": "2.6.9-r0",
      "purl": "pkg:apk/alpine/apk-tools@2.6.9-r0?distro=alpine-3.4.6&upstream=apk-tools&upstream-version=2.6.9-r0",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:e53f74215d12318372e4412d0f0eb3908e17db25c6185f670db49aef5271f91f"
        },
        {
          "name": "sysdig:layer:index",
          "value": "0"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    },
    {
      "bom-ref": "f1b5e225-0db5-41be-bcfa-3ac8a1c90189",
      "type": "library",
      "name": "scanelf",
      "version": "1.1.6-r0",
      "purl": "pkg:apk/alpine/scanelf@1.1.6-r0?distro=alpine-3.4.6&upstream=pax-utils&upstream-version=1.1.6-r0",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:e53f74215d12318372e4412d0f0eb3908e17db25c6185f670db49aef5271f91f"
        },
        {
          "name": "sysdig:layer:index",
          "value": "0"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    },
    {
      "bom-ref": "42a77d43-2513-44d4-b4a4-6874ed539684",
      "type": "library",
      "name": "musl-utils",
      "version": "1.1.14-r16",
      "purl": "pkg:apk/alpine/musl-utils@1.1.14-r16?distro=alpine-3.4.6&upstream=musl&upstream-version=1.1.14-r16",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:e53f74215d12318372e4412d0f0eb3908e17db25c6185f670db49aef5271f91f"
        },
        {
          "name": "sysdig:layer:index",
          "value": "0"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    },
    {
      "bom-ref": "89d56d13-6340-4e83-a268-cd97a79a55d9",
      "type": "library",
      "name": "libc-utils",
      "version": "0.7-r0",
      "purl": "pkg:apk/alpine/libc-utils@0.7-r0?distro=alpine-3.4.6&upstream=libc-dev&upstream-version=0.7-r0",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:e53f74215d12318372e4412d0f0eb3908e17db25c6185f670db49aef5271f91f"
        },
        {
          "name": "sysdig:layer:index",
          "value": "0"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    },
    {
      "bom-ref": "d6263241-33a5-490e-be41-17a02b4eec96",
      "type": "library",
      "name": "libcap",
      "version": "2.25-r0",
      "purl": "pkg:apk/alpine/libcap@2.25-r0?distro=alpine-3.4.6&upstream=libcap&upstream-version=2.25-r0",
      "properties": [
        {
          "name": "sysdig:layer:digest",
          "value": "sha256:36cb79cf24181202e273049789e8dbfe4b5eb2258ecf4e923ac4a4a9a05d9380"
        },
        {
          "name": "sysdig:layer:index",
          "value": "1"
        },
        {
          "name": "sysdig:package:installPath",
          "value": "/lib/apk/db/installed"
        }
      ]
    }
  ],
  "dependencies": [
    {
      "ref": "243be7c9-ea6e-4a4f-823f-76a68478137b",
      "dependsOn": [
        "77bf9328-4e89-4115-8a4c-1d0090a09bfd"
      ]
    }
  ]
}
 ```

### resources
https://www.youtube.com/watch?v=sC9zE5pGl_Y
