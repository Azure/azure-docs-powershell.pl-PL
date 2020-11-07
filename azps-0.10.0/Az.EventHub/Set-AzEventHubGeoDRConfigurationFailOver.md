---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Set-AzEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 6569c5081ec92e20682edf63c09f1b4319d4c038
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891410"
---
# <span data-ttu-id="72244-101">Set-AzEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="72244-101">Set-AzEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="72244-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72244-102">SYNOPSIS</span></span>
<span data-ttu-id="72244-103">Wywołuje tryb failover w trybie GEO DR i ponownie skonfiguruje alias tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="72244-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="72244-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72244-104">SYNTAX</span></span>

### <span data-ttu-id="72244-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72244-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72244-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="72244-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72244-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72244-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72244-108">Opis</span><span class="sxs-lookup"><span data-stu-id="72244-108">DESCRIPTION</span></span>
<span data-ttu-id="72244-109">Polecenie cmdlet **Set-AzEventHubGeoDRConfigurationFailOver** umożliwia przełączenie do trybu failover w trybie Geo i ponowne skonfigurowanie aliasu tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="72244-109">The **Set-AzEventHubGeoDRConfigurationFailOver** cmdlet invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="72244-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72244-110">EXAMPLES</span></span>

### <span data-ttu-id="72244-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72244-111">Example 1</span></span>
```
PS C:\>Set-AzEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRConfigName"
```

<span data-ttu-id="72244-112">Wywołuje tryb failover na aliasie "SampleDRConfigName", ponownie konfiguruje i wskazuje pomocniczy obszar nazw "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="72244-112">Invokes the Failover over alias "SampleDRConfigName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="72244-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72244-113">PARAMETERS</span></span>

### <span data-ttu-id="72244-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72244-114">-DefaultProfile</span></span>
<span data-ttu-id="72244-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72244-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72244-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="72244-116">-InputObject</span></span>
<span data-ttu-id="72244-117">Obiekt konfiguracji GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="72244-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="72244-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72244-118">-Name</span></span>
<span data-ttu-id="72244-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="72244-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="72244-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="72244-120">-Namespace</span></span>
<span data-ttu-id="72244-121">Nazwa przestrzeni nazw — pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="72244-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="72244-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72244-122">-PassThru</span></span>
<span data-ttu-id="72244-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="72244-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="72244-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="72244-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="72244-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72244-125">-ResourceGroupName</span></span>
<span data-ttu-id="72244-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="72244-126">Resource Group Name</span></span>

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

### <span data-ttu-id="72244-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72244-127">-ResourceId</span></span>
<span data-ttu-id="72244-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="72244-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="72244-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72244-129">-Confirm</span></span>
<span data-ttu-id="72244-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72244-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72244-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72244-131">-WhatIf</span></span>
<span data-ttu-id="72244-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72244-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72244-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72244-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72244-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72244-134">CommonParameters</span></span>
<span data-ttu-id="72244-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72244-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72244-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72244-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72244-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72244-137">INPUTS</span></span>

### <span data-ttu-id="72244-138">System. String</span><span class="sxs-lookup"><span data-stu-id="72244-138">System.String</span></span>

### <span data-ttu-id="72244-139">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="72244-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>

## <span data-ttu-id="72244-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72244-140">OUTPUTS</span></span>

### <span data-ttu-id="72244-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72244-141">System.Boolean</span></span>

## <span data-ttu-id="72244-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72244-142">NOTES</span></span>

## <span data-ttu-id="72244-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72244-143">RELATED LINKS</span></span>
