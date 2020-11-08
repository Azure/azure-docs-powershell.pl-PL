---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: f343b92452a34a746d9ff09d5a519519aeaa7a6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231907"
---
# <span data-ttu-id="cf021-101">Set-AzEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="cf021-101">Set-AzEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="cf021-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cf021-102">SYNOPSIS</span></span>
<span data-ttu-id="cf021-103">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="cf021-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="cf021-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cf021-104">SYNTAX</span></span>

### <span data-ttu-id="cf021-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cf021-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf021-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cf021-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf021-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf021-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf021-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cf021-108">DESCRIPTION</span></span>
<span data-ttu-id="cf021-109">Polecenie cmdlet **Set-AzEventHubGeoDRConfigurationBreakPair** wyłącza odzyskiwanie po awarii i zatrzymuje Replikowanie zmian z podstawowych do pomocniczych obszarów nazw</span><span class="sxs-lookup"><span data-stu-id="cf021-109">The **Set-AzEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="cf021-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cf021-110">EXAMPLES</span></span>

### <span data-ttu-id="cf021-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cf021-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRConfigName"
```

<span data-ttu-id="cf021-112">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="cf021-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="cf021-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cf021-113">PARAMETERS</span></span>

### <span data-ttu-id="cf021-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf021-114">-DefaultProfile</span></span>
<span data-ttu-id="cf021-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cf021-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf021-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cf021-116">-InputObject</span></span>
<span data-ttu-id="cf021-117">Obiekt konfiguracji GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="cf021-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="cf021-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cf021-118">-Name</span></span>
<span data-ttu-id="cf021-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="cf021-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="cf021-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="cf021-120">-Namespace</span></span>
<span data-ttu-id="cf021-121">Nazwa obszaru nazw — podstawowy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="cf021-121">Namespace Name - Primary Namespace</span></span>

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

### <span data-ttu-id="cf021-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf021-122">-PassThru</span></span>
<span data-ttu-id="cf021-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="cf021-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf021-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="cf021-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf021-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf021-125">-ResourceGroupName</span></span>
<span data-ttu-id="cf021-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="cf021-126">Resource Group Name</span></span>

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

### <span data-ttu-id="cf021-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf021-127">-ResourceId</span></span>
<span data-ttu-id="cf021-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf021-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="cf021-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cf021-129">-Confirm</span></span>
<span data-ttu-id="cf021-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf021-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf021-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf021-131">-WhatIf</span></span>
<span data-ttu-id="cf021-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf021-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf021-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cf021-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf021-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf021-134">CommonParameters</span></span>
<span data-ttu-id="cf021-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf021-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf021-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf021-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf021-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cf021-137">INPUTS</span></span>

### <span data-ttu-id="cf021-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cf021-138">System.String</span></span>

### <span data-ttu-id="cf021-139">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="cf021-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="cf021-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cf021-140">OUTPUTS</span></span>

### <span data-ttu-id="cf021-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cf021-141">System.Boolean</span></span>

## <span data-ttu-id="cf021-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cf021-142">NOTES</span></span>

## <span data-ttu-id="cf021-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cf021-143">RELATED LINKS</span></span>
