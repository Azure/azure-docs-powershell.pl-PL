---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: 871f3ba59fb84cea10200a7983fe7ee80b68918e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501358"
---
# <span data-ttu-id="fefda-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="fefda-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="fefda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fefda-102">SYNOPSIS</span></span>
<span data-ttu-id="fefda-103">Dodaj lub zaktualizuj jedną lub wiele ustawień sieci szkieletowej usług do klastra.</span><span class="sxs-lookup"><span data-stu-id="fefda-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="fefda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fefda-104">SYNTAX</span></span>

### <span data-ttu-id="fefda-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="fefda-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fefda-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="fefda-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fefda-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fefda-107">DESCRIPTION</span></span>
<span data-ttu-id="fefda-108">Aby dodać lub zaktualizować ustawienia sieci szkieletowej usług w klastrze, użyj **Ustawienia Set-AzServiceFabricSetting** .</span><span class="sxs-lookup"><span data-stu-id="fefda-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="fefda-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fefda-109">EXAMPLES</span></span>

### <span data-ttu-id="fefda-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fefda-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="fefda-111">W tym poleceniu w sekcji "NamingService" zostanie ustawiona wartość "MaxFileOperationTimeout" równa "5000".</span><span class="sxs-lookup"><span data-stu-id="fefda-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="fefda-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fefda-112">Example 2</span></span>
```
$fabricSettings = @(
    @{ 
        "name" = "NamingService";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "MaxFileOperationTimeout"; "Value" = "5000"  };
            @{ "Name" = "MaxOperationTimeout"; "Value" = "1200"  })
    },
    @{ 
        "name" = "Hosting";
        "parameters" =  [System.Collections.Generic.List[Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsParameterDescription]]@(
            @{ "Name" = "ActivationMaxFailureCount"; "Value" = "11"  })
    })

Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -SettingsSectionDescription $fabricSettings -Verbose
```

<span data-ttu-id="fefda-113">To polecenie wyzwoli uaktualnienie w celu ustawienia wielu ustawień sieci szkieletowej przy użyciu parametru SettingsSectionDescription.</span><span class="sxs-lookup"><span data-stu-id="fefda-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="fefda-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fefda-114">PARAMETERS</span></span>

### <span data-ttu-id="fefda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fefda-115">-DefaultProfile</span></span>
<span data-ttu-id="fefda-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fefda-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fefda-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fefda-117">-Name</span></span>
<span data-ttu-id="fefda-118">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="fefda-118">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fefda-119">-Parameter</span><span class="sxs-lookup"><span data-stu-id="fefda-119">-Parameter</span></span>
<span data-ttu-id="fefda-120">Nazwa parametru ustawienia sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="fefda-120">Parameter name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fefda-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fefda-121">-ResourceGroupName</span></span>
<span data-ttu-id="fefda-122">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fefda-122">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fefda-123">Sekcja</span><span class="sxs-lookup"><span data-stu-id="fefda-123">-Section</span></span>
<span data-ttu-id="fefda-124">Nazwa sekcji Ustawienia sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="fefda-124">Section name of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fefda-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="fefda-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="fefda-126">Tablica ustawień sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="fefda-126">An array of fabric settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fefda-127">-Value</span><span class="sxs-lookup"><span data-stu-id="fefda-127">-Value</span></span>
<span data-ttu-id="fefda-128">Wartość parametru ustawienia sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="fefda-128">Parameter value of the fabric setting</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fefda-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fefda-129">-Confirm</span></span>
<span data-ttu-id="fefda-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fefda-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fefda-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fefda-131">-WhatIf</span></span>
<span data-ttu-id="fefda-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fefda-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fefda-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fefda-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fefda-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fefda-134">CommonParameters</span></span>
<span data-ttu-id="fefda-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fefda-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fefda-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fefda-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fefda-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fefda-137">INPUTS</span></span>

### <span data-ttu-id="fefda-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fefda-138">System.String</span></span>

### <span data-ttu-id="fefda-139">Microsoft. Azure. Commands. servicefabric. MODELES. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="fefda-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="fefda-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fefda-140">OUTPUTS</span></span>

### <span data-ttu-id="fefda-141">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="fefda-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="fefda-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fefda-142">NOTES</span></span>

## <span data-ttu-id="fefda-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fefda-143">RELATED LINKS</span></span>
