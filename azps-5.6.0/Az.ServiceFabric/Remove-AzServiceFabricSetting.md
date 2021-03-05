---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 2df7c5f6af50bf581963f08e0544eb453f4b27df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005402"
---
# <span data-ttu-id="a05d4-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="a05d4-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="a05d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a05d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a05d4-103">Usuń jedno lub wiele ustawień usługi Fabric z klastrów.</span><span class="sxs-lookup"><span data-stu-id="a05d4-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="a05d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a05d4-104">SYNTAX</span></span>

### <span data-ttu-id="a05d4-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="a05d4-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a05d4-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="a05d4-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a05d4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a05d4-107">DESCRIPTION</span></span>
<span data-ttu-id="a05d4-108">Użyj **ustawienia Remove-AzServiceFabricSetting,** aby usunąć ustawienia usługi Fabric z klastru.</span><span class="sxs-lookup"><span data-stu-id="a05d4-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="a05d4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a05d4-109">EXAMPLES</span></span>

### <span data-ttu-id="a05d4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a05d4-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="a05d4-111">To polecenie spowoduje usunięcie ustawień "MaxCursors" w sekcji "EseStore".</span><span class="sxs-lookup"><span data-stu-id="a05d4-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="a05d4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a05d4-112">PARAMETERS</span></span>

### <span data-ttu-id="a05d4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05d4-113">-DefaultProfile</span></span>
<span data-ttu-id="a05d4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a05d4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a05d4-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a05d4-115">-Name</span></span>
<span data-ttu-id="a05d4-116">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="a05d4-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="a05d4-117">- Parametr</span><span class="sxs-lookup"><span data-stu-id="a05d4-117">-Parameter</span></span>
<span data-ttu-id="a05d4-118">Nazwa parametru ustawienia materiału</span><span class="sxs-lookup"><span data-stu-id="a05d4-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="a05d4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05d4-119">-ResourceGroupName</span></span>
<span data-ttu-id="a05d4-120">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a05d4-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a05d4-121">— Sekcja</span><span class="sxs-lookup"><span data-stu-id="a05d4-121">-Section</span></span>
<span data-ttu-id="a05d4-122">Nazwa sekcji ustawienia materiału</span><span class="sxs-lookup"><span data-stu-id="a05d4-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="a05d4-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="a05d4-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="a05d4-124">Tablica ustawień materiału</span><span class="sxs-lookup"><span data-stu-id="a05d4-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="a05d4-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a05d4-125">-Confirm</span></span>
<span data-ttu-id="a05d4-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a05d4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a05d4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a05d4-127">-WhatIf</span></span>
<span data-ttu-id="a05d4-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a05d4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a05d4-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a05d4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a05d4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05d4-130">CommonParameters</span></span>
<span data-ttu-id="a05d4-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a05d4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05d4-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a05d4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05d4-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a05d4-133">INPUTS</span></span>

### <span data-ttu-id="a05d4-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a05d4-134">System.String</span></span>

### <span data-ttu-id="a05d4-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span><span class="sxs-lookup"><span data-stu-id="a05d4-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="a05d4-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a05d4-136">OUTPUTS</span></span>

### <span data-ttu-id="a05d4-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="a05d4-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a05d4-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a05d4-138">NOTES</span></span>

## <span data-ttu-id="a05d4-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a05d4-139">RELATED LINKS</span></span>
