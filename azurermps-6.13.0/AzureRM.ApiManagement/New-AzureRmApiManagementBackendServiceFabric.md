---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
ms.openlocfilehash: 925e4949b444c9338fad3f88cf5066430e1b5a75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542039"
---
# <span data-ttu-id="10a8f-101">New-AzureRmApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10a8f-101">New-AzureRmApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="10a8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="10a8f-103">Tworzy obiekt `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="10a8f-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10a8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10a8f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint <String[]>
 -ClientCertificateThumbprint <String> [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>]
 [-ServerCertificateThumbprint <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10a8f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="10a8f-105">DESCRIPTION</span></span>

<span data-ttu-id="10a8f-106">Polecenie cmdlet **New-AzureRmApiManagementBackendServiceFabric** tworzy obiekt, którego `PsApiManagementServiceFabric` należy użyć w polecenia cmdlet **New-AzureRmApiManagementBackend** and **Set-AzureRmApiManagementBackend**.</span><span class="sxs-lookup"><span data-stu-id="10a8f-106">The **New-AzureRmApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzureRmApiManagementBackend** and **Set-AzureRmApiManagementBackend**.</span></span>

## <span data-ttu-id="10a8f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10a8f-107">EXAMPLES</span></span>

### <span data-ttu-id="10a8f-108">Przykład 1. Tworzenie obiektu In-Memory usługi sieci szkieletowej zaplecza</span><span class="sxs-lookup"><span data-stu-id="10a8f-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="10a8f-109">Tworzenie kontraktu sieci szkieletowej usługi wewnętrznej bazy danych</span><span class="sxs-lookup"><span data-stu-id="10a8f-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="10a8f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10a8f-110">PARAMETERS</span></span>

### <span data-ttu-id="10a8f-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="10a8f-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="10a8f-112">Odcisk palca certyfikatu klienta dla punktu końcowego zarządzania.</span><span class="sxs-lookup"><span data-stu-id="10a8f-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="10a8f-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="10a8f-113">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a8f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a8f-114">-DefaultProfile</span></span>
<span data-ttu-id="10a8f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10a8f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10a8f-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="10a8f-116">-ManagementEndpoint</span></span>
<span data-ttu-id="10a8f-117">Punkty końcowe zarządzania klastrem usługi Fabric.</span><span class="sxs-lookup"><span data-stu-id="10a8f-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="10a8f-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="10a8f-118">This parameter is required.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10a8f-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="10a8f-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="10a8f-120">Maksymalna liczba ponownych prób podczas rozpoznawania partycji programu Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="10a8f-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="10a8f-121">Ten parametr jest opcjonalny i wartością domyślną jest 5.</span><span class="sxs-lookup"><span data-stu-id="10a8f-121">This parameter is optional and default value is 5.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10a8f-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="10a8f-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="10a8f-123">Odcisk palca certyfikatów, które usługa zarządzania klastrami używa do komunikacji TLS. Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="10a8f-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10a8f-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="10a8f-124">-ServerX509Name</span></span>
<span data-ttu-id="10a8f-125">Kolekcja nazw certyfikatów x509 serwera.</span><span class="sxs-lookup"><span data-stu-id="10a8f-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="10a8f-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="10a8f-126">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10a8f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a8f-127">CommonParameters</span></span>
<span data-ttu-id="10a8f-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10a8f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a8f-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10a8f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a8f-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10a8f-130">INPUTS</span></span>

### <span data-ttu-id="10a8f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="10a8f-131">System.String</span></span>

## <span data-ttu-id="10a8f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10a8f-132">OUTPUTS</span></span>

### <span data-ttu-id="10a8f-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10a8f-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="10a8f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10a8f-134">NOTES</span></span>

## <span data-ttu-id="10a8f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10a8f-135">RELATED LINKS</span></span>

[<span data-ttu-id="10a8f-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="10a8f-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="10a8f-137">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="10a8f-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="10a8f-138">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="10a8f-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="10a8f-139">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="10a8f-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="10a8f-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="10a8f-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
