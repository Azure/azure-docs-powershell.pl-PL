---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/stop-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Stop-AzureRmServiceBusMigration.md
ms.openlocfilehash: 25a8b6918c5cd10a2f47230274c357008731ffba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546459"
---
# <span data-ttu-id="94bbc-101">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="94bbc-101">Stop-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="94bbc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="94bbc-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="94bbc-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94bbc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94bbc-104">SYNTAX</span></span>

### <span data-ttu-id="94bbc-105">MigrationConfigurationPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="94bbc-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94bbc-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="94bbc-106">NamespaceInputObjectSet</span></span>
```
Stop-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94bbc-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94bbc-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94bbc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="94bbc-108">DESCRIPTION</span></span>
<span data-ttu-id="94bbc-109">Polecenia cmdlet **stop-AzureRmServiceBusMigration** tremitates migrację między standardowym obszarem nazw Premium</span><span class="sxs-lookup"><span data-stu-id="94bbc-109">The **Stop-AzureRmServiceBusMigration** cmdlets  tremitates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="94bbc-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94bbc-110">EXAMPLES</span></span>

### <span data-ttu-id="94bbc-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94bbc-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="94bbc-112">polecenie cmdlet termitates migrację między standardowym obszarem nazw a obszarem nazw Premium, które podano podczas tworzenia konfiguracji migracji.</span><span class="sxs-lookup"><span data-stu-id="94bbc-112">cmdlet termitates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="94bbc-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94bbc-113">PARAMETERS</span></span>

### <span data-ttu-id="94bbc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94bbc-114">-DefaultProfile</span></span>
<span data-ttu-id="94bbc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94bbc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94bbc-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="94bbc-116">-InputObject</span></span>
<span data-ttu-id="94bbc-117">Obiekt Namespace konfiguracji migracji usługi Service Bus Standard</span><span class="sxs-lookup"><span data-stu-id="94bbc-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94bbc-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="94bbc-118">-Name</span></span>
<span data-ttu-id="94bbc-119">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="94bbc-119">Standard Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94bbc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94bbc-120">-PassThru</span></span>
<span data-ttu-id="94bbc-121">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="94bbc-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="94bbc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94bbc-122">-ResourceGroupName</span></span>
<span data-ttu-id="94bbc-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="94bbc-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94bbc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94bbc-124">-ResourceId</span></span>
<span data-ttu-id="94bbc-125">Identyfikator zasobu standardowej przestrzeni nazw konfiguracji migracji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="94bbc-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94bbc-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94bbc-126">-Confirm</span></span>
<span data-ttu-id="94bbc-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94bbc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94bbc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94bbc-128">-WhatIf</span></span>
<span data-ttu-id="94bbc-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94bbc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94bbc-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="94bbc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94bbc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94bbc-131">CommonParameters</span></span>
<span data-ttu-id="94bbc-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94bbc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94bbc-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94bbc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94bbc-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94bbc-134">INPUTS</span></span>

### <span data-ttu-id="94bbc-135">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="94bbc-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="94bbc-136">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="94bbc-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="94bbc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="94bbc-137">System.String</span></span>

## <span data-ttu-id="94bbc-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94bbc-138">OUTPUTS</span></span>

### <span data-ttu-id="94bbc-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94bbc-139">System.Boolean</span></span>

## <span data-ttu-id="94bbc-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94bbc-140">NOTES</span></span>

## <span data-ttu-id="94bbc-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94bbc-141">RELATED LINKS</span></span>
