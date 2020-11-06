---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusMigration.md
ms.openlocfilehash: c378f6315f66b7149c1a8bb6d51ce806425065a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543424"
---
# <span data-ttu-id="246aa-101">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="246aa-101">Remove-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="246aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="246aa-102">SYNOPSIS</span></span>
<span data-ttu-id="246aa-103">Polecenie cmdlet usuwa konfigurację migracji dla obszarów nazw standardowych do Premium</span><span class="sxs-lookup"><span data-stu-id="246aa-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="246aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="246aa-104">SYNTAX</span></span>

### <span data-ttu-id="246aa-105">MigrationConfigurationPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="246aa-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="246aa-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="246aa-106">NamespaceInputObjectSet</span></span>
```
Remove-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="246aa-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="246aa-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="246aa-108">Opis</span><span class="sxs-lookup"><span data-stu-id="246aa-108">DESCRIPTION</span></span>
<span data-ttu-id="246aa-109">Polecenie cmdlet **Remove-AzureRmServiceBusMigration** usuwa konfigurację migracji dla obszarów nazw standardowych do Premium</span><span class="sxs-lookup"><span data-stu-id="246aa-109">The **Remove-AzureRmServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="246aa-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="246aa-110">EXAMPLES</span></span>

### <span data-ttu-id="246aa-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="246aa-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation
```

<span data-ttu-id="246aa-112">Usuwa konfigurację migracji "TestingNamespaceStandardMirgation"</span><span class="sxs-lookup"><span data-stu-id="246aa-112">Deletes the 'TestingNamespaceStandardMirgation' migration configuration</span></span>

## <span data-ttu-id="246aa-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="246aa-113">PARAMETERS</span></span>

### <span data-ttu-id="246aa-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="246aa-114">-AsJob</span></span>
<span data-ttu-id="246aa-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="246aa-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="246aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="246aa-116">-DefaultProfile</span></span>
<span data-ttu-id="246aa-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="246aa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="246aa-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="246aa-118">-InputObject</span></span>
<span data-ttu-id="246aa-119">Obiekt przestrzeni nazw standardowego migracji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="246aa-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="246aa-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="246aa-120">-Name</span></span>
<span data-ttu-id="246aa-121">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="246aa-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="246aa-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="246aa-122">-PassThru</span></span>
<span data-ttu-id="246aa-123">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="246aa-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="246aa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="246aa-124">-ResourceGroupName</span></span>
<span data-ttu-id="246aa-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="246aa-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="246aa-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="246aa-126">-ResourceId</span></span>
<span data-ttu-id="246aa-127">Identyfikator zasobu standardowej przestrzeni nazw migracji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="246aa-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="246aa-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="246aa-128">-Confirm</span></span>
<span data-ttu-id="246aa-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="246aa-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="246aa-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="246aa-130">-WhatIf</span></span>
<span data-ttu-id="246aa-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="246aa-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="246aa-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="246aa-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="246aa-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="246aa-133">CommonParameters</span></span>
<span data-ttu-id="246aa-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="246aa-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="246aa-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="246aa-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="246aa-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="246aa-136">INPUTS</span></span>

### <span data-ttu-id="246aa-137">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="246aa-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="246aa-138">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="246aa-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="246aa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="246aa-139">System.String</span></span>

## <span data-ttu-id="246aa-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="246aa-140">OUTPUTS</span></span>

### <span data-ttu-id="246aa-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="246aa-141">System.Boolean</span></span>

## <span data-ttu-id="246aa-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="246aa-142">NOTES</span></span>

## <span data-ttu-id="246aa-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="246aa-143">RELATED LINKS</span></span>
