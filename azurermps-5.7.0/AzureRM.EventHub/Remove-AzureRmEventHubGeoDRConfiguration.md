---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubGeodrconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubGeoDRConfiguration.md
ms.openlocfilehash: 929ebdfb9cc38d5233027da75752f4c82c484536
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545740"
---
# <span data-ttu-id="1fb54-101">Remove-AzureRmEventHubGeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fb54-101">Remove-AzureRmEventHubGeoDRConfiguration</span></span>

## <span data-ttu-id="1fb54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fb54-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb54-103">Usuwanie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="1fb54-103">Deletes an Alias(Disaster Recovery configuration)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1fb54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fb54-104">SYNTAX</span></span>

### <span data-ttu-id="1fb54-105">GeoDRParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1fb54-105">GeoDRParameterSet (Default)</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb54-106">GeoDRConfigurationInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1fb54-106">GeoDRConfigurationInputObjectSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-InputObject] <PSEventHubDRConfigurationAttributes> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb54-107">GeoDRConfigResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fb54-107">GeoDRConfigResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubGeoDRConfiguration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fb54-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1fb54-108">DESCRIPTION</span></span>
<span data-ttu-id="1fb54-109">Polecenie cmdlet **Remove-AzureRmEventHubGeoDRConfiguration** umożliwia usunięcie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="1fb54-109">The **Remove-AzureRmEventHubGeoDRConfiguration** cmdlet deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="1fb54-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fb54-110">EXAMPLES</span></span>

### <span data-ttu-id="1fb54-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1fb54-111">Example 1</span></span>
```
PS C:\>Remove-AzureRmEventHubGeoDRConfiguration -ResourceGroupName "SampleResourceGroup" -Namespace "SampleNamespace_Secondary" -Name "SampleDRCongifName"
```

<span data-ttu-id="1fb54-112">Usuwanie aliasu (konfiguracji odzyskiwania po awarii)</span><span class="sxs-lookup"><span data-stu-id="1fb54-112">Deletes an Alias(Disaster Recovery configuration)</span></span>

## <span data-ttu-id="1fb54-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fb54-113">PARAMETERS</span></span>

### <span data-ttu-id="1fb54-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fb54-114">-AsJob</span></span>
<span data-ttu-id="1fb54-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1fb54-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fb54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb54-116">-DefaultProfile</span></span>
<span data-ttu-id="1fb54-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb54-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb54-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1fb54-118">-InputObject</span></span>
<span data-ttu-id="1fb54-119">Obiekt konfiguracji GeoDR Eventhub</span><span class="sxs-lookup"><span data-stu-id="1fb54-119">Eventhub GeoDR Configuration Object</span></span>

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

### <span data-ttu-id="1fb54-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1fb54-120">-Name</span></span>
<span data-ttu-id="1fb54-121">Alias (GeoDR)</span><span class="sxs-lookup"><span data-stu-id="1fb54-121">Alias (GeoDR)</span></span>

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

### <span data-ttu-id="1fb54-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="1fb54-122">-Namespace</span></span>
<span data-ttu-id="1fb54-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="1fb54-123">Namespace Name</span></span>

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

### <span data-ttu-id="1fb54-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fb54-124">-PassThru</span></span>
<span data-ttu-id="1fb54-125">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1fb54-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1fb54-126">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1fb54-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1fb54-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fb54-127">-ResourceGroupName</span></span>
<span data-ttu-id="1fb54-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1fb54-128">Resource Group Name</span></span>

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

### <span data-ttu-id="1fb54-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fb54-129">-ResourceId</span></span>
<span data-ttu-id="1fb54-130">Identyfikator zasobu GeoDRConfiguration</span><span class="sxs-lookup"><span data-stu-id="1fb54-130">GeoDRConfiguration Resource Id</span></span>

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

### <span data-ttu-id="1fb54-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1fb54-131">-Confirm</span></span>
<span data-ttu-id="1fb54-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fb54-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fb54-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fb54-133">-WhatIf</span></span>
<span data-ttu-id="1fb54-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fb54-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fb54-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1fb54-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fb54-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb54-136">CommonParameters</span></span>
<span data-ttu-id="1fb54-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb54-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1fb54-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb54-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb54-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fb54-139">INPUTS</span></span>

### <span data-ttu-id="1fb54-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb54-140">System.String</span></span>
<span data-ttu-id="1fb54-141">Microsoft. Azure. Commands. EventHub. modele. PSEventHubDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1fb54-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubDRConfigurationAttributes</span></span>


## <span data-ttu-id="1fb54-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fb54-142">OUTPUTS</span></span>

### <span data-ttu-id="1fb54-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fb54-143">System.Boolean</span></span>


## <span data-ttu-id="1fb54-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fb54-144">NOTES</span></span>

## <span data-ttu-id="1fb54-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fb54-145">RELATED LINKS</span></span>
