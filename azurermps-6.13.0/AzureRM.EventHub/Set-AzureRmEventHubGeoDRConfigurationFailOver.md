---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubgeodrconfigurationfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubGeoDRConfigurationFailOver.md
ms.openlocfilehash: 84a101a427fc5541d4888a0b4deb4c5e3880b1d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545339"
---
# <span data-ttu-id="8e016-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span><span class="sxs-lookup"><span data-stu-id="8e016-101">Set-AzureRmEventHubGeoDRConfigurationFailOver</span></span>

## <span data-ttu-id="8e016-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e016-102">SYNOPSIS</span></span>
<span data-ttu-id="8e016-103">Wywołuje tryb failover w trybie GEO DR i ponownie skonfiguruje alias tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="8e016-103">Invokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e016-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e016-104">SYNTAX</span></span>

### <span data-ttu-id="8e016-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8e016-105">GeoDRParameterSet (Default)</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceGroupName] <String> [-Namespace] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e016-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8e016-106">GeoDRConfigurationInputObjectSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e016-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e016-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Set-AzureRmEventHubGeoDRConfigurationFailOver [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e016-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8e016-108">DESCRIPTION</span></span>
<span data-ttu-id="8e016-109">Polecenie cmdlet **Set-AzureRmEventHubGeoDRConfigurationFailOver** ENVOKES Geo Dr failover oraz Zmień konfigurację aliasu tak, aby wskazywał pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="8e016-109">The **Set-AzureRmEventHubGeoDRConfigurationFailOver** cmdlet envokes GEO DR failover and reconfigure the alias to point to the secondary namespace</span></span>

## <span data-ttu-id="8e016-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e016-110">EXAMPLES</span></span>

### <span data-ttu-id="8e016-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e016-111">Example 1</span></span>
```
PS C:\>Set-AzureRmEventHubGeoDRConfigurationFailOver -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="8e016-112">Wywołuje tryb failover na aliasie "SampleDRCongifName", ponownie konfiguruje i wskazuje pomocniczy obszar nazw "SampleNamespace_Secondary"</span><span class="sxs-lookup"><span data-stu-id="8e016-112">Invokes the Failover over alias "SampleDRCongifName", reconfigures and point to Secondary namespace "SampleNamespace_Secondary"</span></span>

## <span data-ttu-id="8e016-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e016-113">PARAMETERS</span></span>

### <span data-ttu-id="8e016-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e016-114">-DefaultProfile</span></span>
<span data-ttu-id="8e016-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e016-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e016-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e016-116">-InputObject</span></span>
<span data-ttu-id="8e016-117">Obiekt konfiguracji GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="8e016-117">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="8e016-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e016-118">-Name</span></span>
<span data-ttu-id="8e016-119">Nazwa konfiguracji DR</span><span class="sxs-lookup"><span data-stu-id="8e016-119">DR Configuration Name</span></span>

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

### <span data-ttu-id="8e016-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8e016-120">-Namespace</span></span>
<span data-ttu-id="8e016-121">Nazwa przestrzeni nazw — pomocniczy obszar nazw</span><span class="sxs-lookup"><span data-stu-id="8e016-121">Namespace Name - Secondary Namespace</span></span>

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

### <span data-ttu-id="8e016-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e016-122">-PassThru</span></span>
<span data-ttu-id="8e016-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="8e016-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8e016-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8e016-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8e016-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e016-125">-ResourceGroupName</span></span>
<span data-ttu-id="8e016-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="8e016-126">Resource Group Name</span></span>

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

### <span data-ttu-id="8e016-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e016-127">-ResourceId</span></span>
<span data-ttu-id="8e016-128">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e016-128">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="8e016-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e016-129">-Confirm</span></span>
<span data-ttu-id="8e016-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e016-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e016-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e016-131">-WhatIf</span></span>
<span data-ttu-id="8e016-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e016-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e016-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e016-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e016-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e016-134">CommonParameters</span></span>
<span data-ttu-id="8e016-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e016-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e016-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e016-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e016-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e016-137">INPUTS</span></span>

### <span data-ttu-id="8e016-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8e016-138">System.String</span></span>

### <span data-ttu-id="8e016-139">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="8e016-139">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>
<span data-ttu-id="8e016-140">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8e016-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="8e016-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e016-141">OUTPUTS</span></span>

### <span data-ttu-id="8e016-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e016-142">System.Boolean</span></span>

## <span data-ttu-id="8e016-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e016-143">NOTES</span></span>

## <span data-ttu-id="8e016-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e016-144">RELATED LINKS</span></span>
