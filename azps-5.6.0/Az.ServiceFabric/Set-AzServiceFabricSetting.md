---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: f98a5efeece2eb1e78479c3f76de62db495c6e43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976330"
---
# <span data-ttu-id="ae6b2-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="ae6b2-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="ae6b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae6b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6b2-103">Dodawanie lub aktualizowanie jednego lub wielu ustawień usługi Fabric do klastrowania.</span><span class="sxs-lookup"><span data-stu-id="ae6b2-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="ae6b2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae6b2-104">SYNTAX</span></span>

### <span data-ttu-id="ae6b2-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="ae6b2-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae6b2-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="ae6b2-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae6b2-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae6b2-107">DESCRIPTION</span></span>
<span data-ttu-id="ae6b2-108">Użyj **ustawienia Set-AzServiceFabricSetting,** aby dodać lub zaktualizować ustawienia usługi Service Fabric w klastrze.</span><span class="sxs-lookup"><span data-stu-id="ae6b2-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="ae6b2-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae6b2-109">EXAMPLES</span></span>

### <span data-ttu-id="ae6b2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae6b2-110">Example 1</span></span>
```
Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="ae6b2-111">To polecenie ustawi wartość "MaxFileOperationTimeout" na "5000" w sekcji "NazewnictwoService".</span><span class="sxs-lookup"><span data-stu-id="ae6b2-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>


### <span data-ttu-id="ae6b2-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ae6b2-112">Example 2</span></span>
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

<span data-ttu-id="ae6b2-113">To polecenie wyzwoli uaktualnienie w celu ustawienia wielu elementów szkieletowych przy użyciu parametru SettingsSectionDescription.</span><span class="sxs-lookup"><span data-stu-id="ae6b2-113">This command will trigger an upgrade to set multiple fabric setting using SettingsSectionDescription parameter.</span></span>

## <span data-ttu-id="ae6b2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae6b2-114">PARAMETERS</span></span>

### <span data-ttu-id="ae6b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6b2-115">-DefaultProfile</span></span>
<span data-ttu-id="ae6b2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae6b2-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ae6b2-117">-Name</span></span>
<span data-ttu-id="ae6b2-118">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="ae6b2-118">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="ae6b2-119">- Parametr</span><span class="sxs-lookup"><span data-stu-id="ae6b2-119">-Parameter</span></span>
<span data-ttu-id="ae6b2-120">Nazwa parametru ustawienia materiału</span><span class="sxs-lookup"><span data-stu-id="ae6b2-120">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="ae6b2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae6b2-121">-ResourceGroupName</span></span>
<span data-ttu-id="ae6b2-122">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae6b2-122">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ae6b2-123">— Sekcja</span><span class="sxs-lookup"><span data-stu-id="ae6b2-123">-Section</span></span>
<span data-ttu-id="ae6b2-124">Nazwa sekcji ustawienia materiału</span><span class="sxs-lookup"><span data-stu-id="ae6b2-124">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="ae6b2-125">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="ae6b2-125">-SettingsSectionDescription</span></span>
<span data-ttu-id="ae6b2-126">Tablica ustawień materiału</span><span class="sxs-lookup"><span data-stu-id="ae6b2-126">An array of fabric settings</span></span>

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

### <span data-ttu-id="ae6b2-127">— Wartość</span><span class="sxs-lookup"><span data-stu-id="ae6b2-127">-Value</span></span>
<span data-ttu-id="ae6b2-128">Wartość parametru ustawienia materiału</span><span class="sxs-lookup"><span data-stu-id="ae6b2-128">Parameter value of the fabric setting</span></span>

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

### <span data-ttu-id="ae6b2-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae6b2-129">-Confirm</span></span>
<span data-ttu-id="ae6b2-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ae6b2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae6b2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae6b2-131">-WhatIf</span></span>
<span data-ttu-id="ae6b2-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae6b2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae6b2-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ae6b2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae6b2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6b2-134">CommonParameters</span></span>
<span data-ttu-id="ae6b2-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae6b2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6b2-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae6b2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6b2-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae6b2-137">INPUTS</span></span>

### <span data-ttu-id="ae6b2-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ae6b2-138">System.String</span></span>

### <span data-ttu-id="ae6b2-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="ae6b2-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="ae6b2-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae6b2-140">OUTPUTS</span></span>

### <span data-ttu-id="ae6b2-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="ae6b2-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ae6b2-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae6b2-142">NOTES</span></span>

## <span data-ttu-id="ae6b2-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae6b2-143">RELATED LINKS</span></span>
