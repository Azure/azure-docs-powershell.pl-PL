---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: 26bbf8e86b1a7f9c4c1951a8bf2b284f8740bd74
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894734"
---
# <span data-ttu-id="dad20-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="dad20-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="dad20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dad20-102">SYNOPSIS</span></span>
<span data-ttu-id="dad20-103">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="dad20-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="dad20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dad20-104">SYNTAX</span></span>

### <span data-ttu-id="dad20-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dad20-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad20-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dad20-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad20-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dad20-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dad20-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dad20-108">DESCRIPTION</span></span>
<span data-ttu-id="dad20-109">Polecenie cmdlet **Set-AzEventHubGeoDRConfigurationBreakPair** wyłącza odzyskiwanie po awarii i zatrzymuje Replikowanie zmian z podstawowych do pomocniczych obszarów nazw</span><span class="sxs-lookup"><span data-stu-id="dad20-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="dad20-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dad20-110">EXAMPLES</span></span>

### <span data-ttu-id="dad20-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dad20-111">Example</span></span>
```
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="dad20-112">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="dad20-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="dad20-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dad20-113">PARAMETERS</span></span>

### <span data-ttu-id="dad20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad20-114">-DefaultProfile</span></span>
<span data-ttu-id="dad20-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dad20-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad20-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dad20-116">-InputObject</span></span>
<span data-ttu-id="dad20-117">Obiekt konfiguracji GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="dad20-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="dad20-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dad20-118">-Name</span></span>
<span data-ttu-id="dad20-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="dad20-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="dad20-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dad20-120">-Namespace</span></span>
<span data-ttu-id="dad20-121">Nazwa obszaru nazw — podstawowy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="dad20-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="dad20-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dad20-122">-PassThru</span></span>
<span data-ttu-id="dad20-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="dad20-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dad20-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="dad20-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dad20-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad20-125">-ResourceGroupName</span></span>
<span data-ttu-id="dad20-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dad20-126">Resource Group Name</span></span>

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

### <span data-ttu-id="dad20-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dad20-127">-ResourceId</span></span>
<span data-ttu-id="dad20-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="dad20-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="dad20-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dad20-129">-Confirm</span></span>
<span data-ttu-id="dad20-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dad20-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad20-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad20-131">-WhatIf</span></span>
<span data-ttu-id="dad20-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dad20-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dad20-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dad20-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad20-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad20-134">CommonParameters</span></span>
<span data-ttu-id="dad20-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad20-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad20-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad20-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad20-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dad20-137">INPUTS</span></span>

### <span data-ttu-id="dad20-138">System. String</span><span class="sxs-lookup"><span data-stu-id="dad20-138">System.String</span></span>

### <span data-ttu-id="dad20-139">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="dad20-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="dad20-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dad20-140">OUTPUTS</span></span>

### <span data-ttu-id="dad20-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dad20-141">System.Boolean</span></span>

## <span data-ttu-id="dad20-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dad20-142">NOTES</span></span>

## <span data-ttu-id="dad20-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dad20-143">RELATED LINKS</span></span>
