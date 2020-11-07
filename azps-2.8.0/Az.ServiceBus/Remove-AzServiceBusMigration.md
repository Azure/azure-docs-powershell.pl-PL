---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 759d857d3e46e0e2211f35f4a5901e8aedb1377d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871595"
---
# <span data-ttu-id="1f873-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="1f873-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="1f873-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f873-102">SYNOPSIS</span></span>
<span data-ttu-id="1f873-103">Polecenie cmdlet usuwa konfigurację migracji dla obszarów nazw standardowych do Premium</span><span class="sxs-lookup"><span data-stu-id="1f873-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="1f873-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f873-104">SYNTAX</span></span>

### <span data-ttu-id="1f873-105">MigrationConfigurationPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1f873-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f873-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1f873-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f873-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f873-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f873-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1f873-108">DESCRIPTION</span></span>
<span data-ttu-id="1f873-109">Polecenie cmdlet **Remove-AzServiceBusMigration** usuwa konfigurację migracji dla obszarów nazw standardowych do Premium</span><span class="sxs-lookup"><span data-stu-id="1f873-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="1f873-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f873-110">EXAMPLES</span></span>

### <span data-ttu-id="1f873-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1f873-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="1f873-112">Usuwa konfigurację migracji "TestingNamespaceStandardMigration"</span><span class="sxs-lookup"><span data-stu-id="1f873-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="1f873-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f873-113">PARAMETERS</span></span>

### <span data-ttu-id="1f873-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f873-114">-AsJob</span></span>
<span data-ttu-id="1f873-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1f873-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f873-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f873-116">-DefaultProfile</span></span>
<span data-ttu-id="1f873-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f873-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f873-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1f873-118">-InputObject</span></span>
<span data-ttu-id="1f873-119">Obiekt przestrzeni nazw standardowego migracji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="1f873-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="1f873-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f873-120">-Name</span></span>
<span data-ttu-id="1f873-121">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="1f873-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="1f873-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f873-122">-PassThru</span></span>
<span data-ttu-id="1f873-123">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="1f873-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1f873-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f873-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f873-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1f873-125">Resource Group Name</span></span>

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

### <span data-ttu-id="1f873-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f873-126">-ResourceId</span></span>
<span data-ttu-id="1f873-127">Identyfikator zasobu standardowej przestrzeni nazw migracji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="1f873-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="1f873-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f873-128">-Confirm</span></span>
<span data-ttu-id="1f873-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f873-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f873-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f873-130">-WhatIf</span></span>
<span data-ttu-id="1f873-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f873-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f873-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f873-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f873-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f873-133">CommonParameters</span></span>
<span data-ttu-id="1f873-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f873-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f873-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f873-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f873-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f873-136">INPUTS</span></span>

### <span data-ttu-id="1f873-137">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="1f873-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="1f873-138">System. String</span><span class="sxs-lookup"><span data-stu-id="1f873-138">System.String</span></span>

## <span data-ttu-id="1f873-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f873-139">OUTPUTS</span></span>

### <span data-ttu-id="1f873-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f873-140">System.Boolean</span></span>

## <span data-ttu-id="1f873-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f873-141">NOTES</span></span>

## <span data-ttu-id="1f873-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f873-142">RELATED LINKS</span></span>
