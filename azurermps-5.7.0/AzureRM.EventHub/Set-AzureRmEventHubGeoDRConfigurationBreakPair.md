---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationbreakpair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationBreakPair.md
ms.openlocfilehash: e6dea50e3cb9933d9c6a8aa141f2df43be0b1a18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717204"
---
# <span data-ttu-id="33751-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span><span class="sxs-lookup"><span data-stu-id="33751-101">Set-AzureRmEventHubGeoDRConfigurationBreakPair</span></span>

## <span data-ttu-id="33751-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33751-102">SYNOPSIS</span></span>
<span data-ttu-id="33751-103">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="33751-103">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33751-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33751-104">SYNTAX</span></span>

### <span data-ttu-id="33751-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="33751-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33751-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="33751-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33751-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="33751-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationBreakPair [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33751-108">Opis</span><span class="sxs-lookup"><span data-stu-id="33751-108">DESCRIPTION</span></span>
<span data-ttu-id="33751-109">Polecenie cmdlet **Set-AzureRmEventHubGeoDRConfigurationBreakPair** wyłącza odzyskiwanie po awarii i zatrzymuje Replikowanie zmian z podstawowych do pomocniczych obszarów nazw</span><span class="sxs-lookup"><span data-stu-id="33751-109">The **Set-AzureRmEventHubGeoDRConfigurationBreakPair** cmdlet disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="33751-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33751-110">EXAMPLES</span></span>

### <span data-ttu-id="33751-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33751-111">Example</span></span>
```
PS C:\> Set-AzureRmEventHubGeoDRConfigurationBreakPair -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Primary" -Name "SampleDRCongifName"
```

<span data-ttu-id="33751-112">Ta operacja powoduje wyłączenie odzyskiwania po awarii i zatrzymanie replikowania zmian z podstawowych na pomocnicze obszary nazw.</span><span class="sxs-lookup"><span data-stu-id="33751-112">This operation disables the Disaster Recovery and stops replicating changes from primary to secondary namespaces</span></span>

## <span data-ttu-id="33751-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33751-113">PARAMETERS</span></span>

### <span data-ttu-id="33751-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33751-114">-DefaultProfile</span></span>
<span data-ttu-id="33751-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33751-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33751-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="33751-116">-InputObject</span></span>
<span data-ttu-id="33751-117">Obiekt konfiguracji GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="33751-117">Eventhub GeoDR Configuration Object</span></span>

```yaml
Type: PSEventHubDRConfigurationAttributes
Parameter Sets: GeoDRConfigurationInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33751-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="33751-118">-Name</span></span>
<span data-ttu-id="33751-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="33751-119">DR Configuration Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33751-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="33751-120">-Namespace</span></span>
<span data-ttu-id="33751-121">Nazwa obszaru nazw — podstawowy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="33751-121">Namespace Name - Primary Namespace</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33751-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33751-122">-PassThru</span></span>
<span data-ttu-id="33751-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="33751-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="33751-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="33751-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33751-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33751-125">-ResourceGroupName</span></span>
<span data-ttu-id="33751-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="33751-126">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: GeoDRParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33751-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33751-127">-ResourceId</span></span>
<span data-ttu-id="33751-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="33751-128">GeoDRConfiguration Resource Id</span></span>

```yaml
Type: String
Parameter Sets: GeoDRConfigResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33751-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33751-129">-Confirm</span></span>
<span data-ttu-id="33751-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33751-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33751-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33751-131">-WhatIf</span></span>
<span data-ttu-id="33751-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33751-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33751-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="33751-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33751-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33751-134">CommonParameters</span></span>
<span data-ttu-id="33751-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33751-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="33751-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33751-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33751-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33751-137">INPUTS</span></span>

### <span data-ttu-id="33751-138">System. String</span><span class="sxs-lookup"><span data-stu-id="33751-138">System.String</span></span>
<span data-ttu-id="33751-139">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="33751-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="33751-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33751-140">OUTPUTS</span></span>

### <span data-ttu-id="33751-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="33751-141">System.Boolean</span></span>


## <span data-ttu-id="33751-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33751-142">NOTES</span></span>

## <span data-ttu-id="33751-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33751-143">RELATED LINKS</span></span>
