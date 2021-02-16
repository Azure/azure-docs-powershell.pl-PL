---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 352e40aa64adf5eea98950ac9271f0237e634ab6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239747"
---
# <span data-ttu-id="12c28-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="12c28-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="12c28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12c28-102">SYNOPSIS</span></span>
<span data-ttu-id="12c28-103">Tworzy obiekt `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="12c28-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="12c28-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="12c28-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12c28-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="12c28-105">DESCRIPTION</span></span>

<span data-ttu-id="12c28-106">Polecenie cmdlet **New-AzApiManagementBackendServiceFabric** tworzy obiekt, który ma być używany w `PsApiManagementServiceFabric` poleceniach cmdlet **New-AzApiManagementBackend** i **Set-AzApiManagementBackend.**</span><span class="sxs-lookup"><span data-stu-id="12c28-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="12c28-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="12c28-107">EXAMPLES</span></span>

### <span data-ttu-id="12c28-108">Przykład 1. Tworzenie struktury szkieletowej usługi zaplecza In-Memory obiektu</span><span class="sxs-lookup"><span data-stu-id="12c28-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="12c28-109">Tworzy umowę na szkielet usług zaplecza</span><span class="sxs-lookup"><span data-stu-id="12c28-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="12c28-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12c28-110">PARAMETERS</span></span>

### <span data-ttu-id="12c28-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="12c28-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="12c28-112">Thumbprint certyfikatu klienta dla punktu końcowego zarządzania.</span><span class="sxs-lookup"><span data-stu-id="12c28-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="12c28-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="12c28-113">This parameter is required.</span></span>

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

### <span data-ttu-id="12c28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c28-114">-DefaultProfile</span></span>
<span data-ttu-id="12c28-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="12c28-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12c28-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="12c28-116">-ManagementEndpoint</span></span>
<span data-ttu-id="12c28-117">Punkty końcowe zarządzania klastrami szkieletów usług.</span><span class="sxs-lookup"><span data-stu-id="12c28-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="12c28-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="12c28-118">This parameter is required.</span></span>

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

### <span data-ttu-id="12c28-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="12c28-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="12c28-120">Maksymalna liczba ponownych prób podczas rozpoznawania partycji service Fabric.</span><span class="sxs-lookup"><span data-stu-id="12c28-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="12c28-121">Ten parametr jest opcjonalny, a wartość domyślna to 5.</span><span class="sxs-lookup"><span data-stu-id="12c28-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="12c28-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="12c28-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="12c28-123">Thumbprint of certificates cluster management service uses for tls communication. Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="12c28-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="12c28-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="12c28-124">-ServerX509Name</span></span>
<span data-ttu-id="12c28-125">Kolekcja nazw certyfikatów serwera X509.</span><span class="sxs-lookup"><span data-stu-id="12c28-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="12c28-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="12c28-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="12c28-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c28-127">CommonParameters</span></span>
<span data-ttu-id="12c28-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c28-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c28-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12c28-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c28-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12c28-130">INPUTS</span></span>

### <span data-ttu-id="12c28-131">System.String</span><span class="sxs-lookup"><span data-stu-id="12c28-131">System.String</span></span>

## <span data-ttu-id="12c28-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12c28-132">OUTPUTS</span></span>

### <span data-ttu-id="12c28-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="12c28-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="12c28-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="12c28-134">NOTES</span></span>

## <span data-ttu-id="12c28-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12c28-135">RELATED LINKS</span></span>

[<span data-ttu-id="12c28-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12c28-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="12c28-137">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12c28-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="12c28-138">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="12c28-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="12c28-139">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12c28-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="12c28-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="12c28-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
