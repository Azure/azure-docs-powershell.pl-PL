---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricSetting.md
ms.openlocfilehash: 943edbccfa8ae8e264d4058deac0407a535c614c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049560"
---
# <span data-ttu-id="c070c-101">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="c070c-101">Remove-AzServiceFabricSetting</span></span>

## <span data-ttu-id="c070c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c070c-102">SYNOPSIS</span></span>
<span data-ttu-id="c070c-103">Usuwanie jednego lub wielu ustawień sieci szkieletowej usług z klastra.</span><span class="sxs-lookup"><span data-stu-id="c070c-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

## <span data-ttu-id="c070c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c070c-104">SYNTAX</span></span>

### <span data-ttu-id="c070c-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="c070c-105">OneSetting</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c070c-106">BatchSettings</span><span class="sxs-lookup"><span data-stu-id="c070c-106">BatchSettings</span></span>
```
Remove-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c070c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c070c-107">DESCRIPTION</span></span>
<span data-ttu-id="c070c-108">Użyj narzędzia **Remove-AzServiceFabricSetting** , aby usunąć ustawienia sieci szkieletowej usług z klastra.</span><span class="sxs-lookup"><span data-stu-id="c070c-108">Use **Remove-AzServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="c070c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c070c-109">EXAMPLES</span></span>

### <span data-ttu-id="c070c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c070c-110">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="c070c-111">To polecenie usunie ustawienia "MaxCursors" w sekcji "EseStore".</span><span class="sxs-lookup"><span data-stu-id="c070c-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="c070c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c070c-112">PARAMETERS</span></span>

### <span data-ttu-id="c070c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c070c-113">-DefaultProfile</span></span>
<span data-ttu-id="c070c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c070c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c070c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c070c-115">-Name</span></span>
<span data-ttu-id="c070c-116">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="c070c-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="c070c-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="c070c-117">-Parameter</span></span>
<span data-ttu-id="c070c-118">Nazwa parametru ustawienia sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="c070c-118">Parameter name of the fabric setting</span></span>

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

### <span data-ttu-id="c070c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c070c-119">-ResourceGroupName</span></span>
<span data-ttu-id="c070c-120">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c070c-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c070c-121">Sekcja</span><span class="sxs-lookup"><span data-stu-id="c070c-121">-Section</span></span>
<span data-ttu-id="c070c-122">Nazwa sekcji Ustawienia sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="c070c-122">Section name of the fabric setting</span></span>

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

### <span data-ttu-id="c070c-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="c070c-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="c070c-124">Tablica ustawień sieci szkieletowej</span><span class="sxs-lookup"><span data-stu-id="c070c-124">An array of fabric settings</span></span>

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

### <span data-ttu-id="c070c-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c070c-125">-Confirm</span></span>
<span data-ttu-id="c070c-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c070c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c070c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c070c-127">-WhatIf</span></span>
<span data-ttu-id="c070c-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c070c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c070c-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c070c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c070c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c070c-130">CommonParameters</span></span>
<span data-ttu-id="c070c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c070c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c070c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c070c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c070c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c070c-133">INPUTS</span></span>

### <span data-ttu-id="c070c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c070c-134">System.String</span></span>

### <span data-ttu-id="c070c-135">Microsoft. Azure. Commands. servicefabric. MODELES. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="c070c-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="c070c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c070c-136">OUTPUTS</span></span>

### <span data-ttu-id="c070c-137">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="c070c-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c070c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c070c-138">NOTES</span></span>

## <span data-ttu-id="c070c-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c070c-139">RELATED LINKS</span></span>
