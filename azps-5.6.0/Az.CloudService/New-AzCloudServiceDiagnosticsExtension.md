---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: a87e9c76b2c083392fc37d74a3ba213dba5881ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969610"
---
# <span data-ttu-id="1e3fe-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1e3fe-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="1e3fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e3fe-102">SYNOPSIS</span></span>
<span data-ttu-id="1e3fe-103">Tworzenie obiektu w pamięci na potrzeby rozszerzenia diagnostyki</span><span class="sxs-lookup"><span data-stu-id="1e3fe-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="1e3fe-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1e3fe-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="1e3fe-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1e3fe-105">DESCRIPTION</span></span>
<span data-ttu-id="1e3fe-106">Tworzenie obiektu w pamięci na potrzeby rozszerzenia diagnostyki</span><span class="sxs-lookup"><span data-stu-id="1e3fe-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="1e3fe-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1e3fe-107">EXAMPLES</span></span>

### <span data-ttu-id="1e3fe-108">Przykład 1. Tworzenie obiektu rozszerzenia diagnostyki</span><span class="sxs-lookup"><span data-stu-id="1e3fe-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="1e3fe-109">To polecenie tworzy obiekt rozszerzenia diagnostyki, który jest używany do tworzenia lub aktualizowania usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="1e3fe-110">Aby uzyskać więcej szczegółowych informacji, zobacz New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="1e3fe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e3fe-111">PARAMETERS</span></span>

### <span data-ttu-id="1e3fe-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1e3fe-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1e3fe-113">Wersja pomocnicza automatycznego uaktualniania.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3fe-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="1e3fe-114">-CloudServiceName</span></span>
<span data-ttu-id="1e3fe-115">Nazwa usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-115">Name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3fe-116">- DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="1e3fe-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="1e3fe-117">Określa konfigurację diagnostyki platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="1e3fe-118">Schemat można pobrać, używając następującego polecenia: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics'). PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd"</span><span class="sxs-lookup"><span data-stu-id="1e3fe-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3fe-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1e3fe-119">-Name</span></span>
<span data-ttu-id="1e3fe-120">Nazwa rozszerzenia diagnostyki.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-120">Name of Diagnostics Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3fe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e3fe-121">-ResourceGroupName</span></span>
<span data-ttu-id="1e3fe-122">Nazwa grupy zasobów usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-122">Resource Group name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3fe-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="1e3fe-123">-RolesAppliedTo</span></span>
<span data-ttu-id="1e3fe-124">Role, do których są stosowane.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-124">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3fe-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1e3fe-125">-StorageAccountKey</span></span>
<span data-ttu-id="1e3fe-126">Klucz konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-126">Storage Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3fe-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1e3fe-127">-StorageAccountName</span></span>
<span data-ttu-id="1e3fe-128">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-128">Name of the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3fe-129">— Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="1e3fe-129">-Subscription</span></span>
<span data-ttu-id="1e3fe-130">Subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-130">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3fe-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1e3fe-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="1e3fe-132">Określa wersję rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-132">Specifies the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e3fe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e3fe-133">CommonParameters</span></span>
<span data-ttu-id="1e3fe-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e3fe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e3fe-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e3fe-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e3fe-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e3fe-136">INPUTS</span></span>

## <span data-ttu-id="1e3fe-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e3fe-137">OUTPUTS</span></span>

### <span data-ttu-id="1e3fe-138">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="1e3fe-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="1e3fe-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1e3fe-139">NOTES</span></span>

<span data-ttu-id="1e3fe-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1e3fe-140">ALIASES</span></span>

## <span data-ttu-id="1e3fe-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e3fe-141">RELATED LINKS</span></span>

