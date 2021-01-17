---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubGeoDRConfiguration.md
ms.openlocfilehash: 57a4ee870e10b04e4c5e58e34122376a790ce6d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386925"
---
# <span data-ttu-id="c9997-101">Remove-AzEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9997-101">Remove-AzEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="c9997-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9997-102">SYNOPSIS</span></span>
<span data-ttu-id="c9997-103">Usuwanie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="c9997-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="c9997-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9997-104">SYNTAX</span></span>

### <span data-ttu-id="c9997-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c9997-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9997-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c9997-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9997-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9997-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9997-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c9997-108">DESCRIPTION</span></span>
<span data-ttu-id="c9997-109">Polecenie cmdlet **Remove-AzEventHubGeoDRConfiguration** umożliwia usunięcie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="c9997-109">The **Remove-AzEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="c9997-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9997-110">EXAMPLES</span></span>

### <span data-ttu-id="c9997-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c9997-111">Example 1</span></span>
```
PS C:\>Remove-AzEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="c9997-112">Usuwanie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="c9997-112">Deletes an Alias (Disaster Recovery configuration)</span></span>

## <span data-ttu-id="c9997-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9997-113">PARAMETERS</span></span>

### <span data-ttu-id="c9997-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9997-114">-AsJob</span></span>
<span data-ttu-id="c9997-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c9997-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9997-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9997-116">-DefaultProfile</span></span>
<span data-ttu-id="c9997-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9997-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9997-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c9997-118">-InputObject</span></span>
<span data-ttu-id="c9997-119">Obiekt konfiguracji GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="c9997-119">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9997-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c9997-120">-Name</span></span>
<span data-ttu-id="c9997-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="c9997-121">Alias (GeoDR)</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9997-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c9997-122">-Namespace</span></span>
<span data-ttu-id="c9997-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="c9997-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9997-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9997-124">-PassThru</span></span>
<span data-ttu-id="c9997-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c9997-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c9997-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c9997-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9997-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9997-127">-ResourceGroupName</span></span>
<span data-ttu-id="c9997-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c9997-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9997-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9997-129">-ResourceId</span></span>
<span data-ttu-id="c9997-130">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9997-130">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9997-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9997-131">-Confirm</span></span>
<span data-ttu-id="c9997-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9997-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9997-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9997-133">-WhatIf</span></span>
<span data-ttu-id="c9997-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9997-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9997-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9997-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9997-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9997-136">CommonParameters</span></span>
<span data-ttu-id="c9997-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9997-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9997-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9997-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9997-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9997-139">INPUTS</span></span>

### <span data-ttu-id="c9997-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c9997-140">System.String</span></span>

### <span data-ttu-id="c9997-141">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="c9997-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="c9997-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9997-142">OUTPUTS</span></span>

### <span data-ttu-id="c9997-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9997-143">System.Boolean</span></span>

## <span data-ttu-id="c9997-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9997-144">NOTES</span></span>

## <span data-ttu-id="c9997-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9997-145">RELATED LINKS</span></span>
