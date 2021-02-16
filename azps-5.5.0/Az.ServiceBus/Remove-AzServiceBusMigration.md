---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusMigration.md
ms.openlocfilehash: 42bb6a61e2298c43cb0828a031495b086b46c9d2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201634"
---
# <span data-ttu-id="93ce0-101">Remove-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="93ce0-101">Remove-AzServiceBusMigration</span></span>

## <span data-ttu-id="93ce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="93ce0-103">Polecenie cmdlet usuwa konfigurację migracji przestrzeni nazw Typu Standard do Premium</span><span class="sxs-lookup"><span data-stu-id="93ce0-103">Cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="93ce0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="93ce0-104">SYNTAX</span></span>

### <span data-ttu-id="93ce0-105">MigrationConfigurationPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="93ce0-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93ce0-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="93ce0-106">NamespaceInputObjectSet</span></span>
```
Remove-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93ce0-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93ce0-107">NamespaceResourceIdParameterSet</span></span>
```
Remove-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93ce0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="93ce0-108">DESCRIPTION</span></span>
<span data-ttu-id="93ce0-109">Polecenie **cmdlet Remove-AzServiceBusMigration** usuwa konfigurację migracji przestrzeni nazw Standard do Premium</span><span class="sxs-lookup"><span data-stu-id="93ce0-109">The **Remove-AzServiceBusMigration** cmdlet deletes the Migration configuration for Standard to Premium namespaces</span></span>

## <span data-ttu-id="93ce0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="93ce0-110">EXAMPLES</span></span>

### <span data-ttu-id="93ce0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="93ce0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="93ce0-112">Usuwa konfigurację migracji "TestingNamespaceStandardMigration"</span><span class="sxs-lookup"><span data-stu-id="93ce0-112">Deletes the 'TestingNamespaceStandardMigration' migration configuration</span></span>

## <span data-ttu-id="93ce0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93ce0-113">PARAMETERS</span></span>

### <span data-ttu-id="93ce0-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="93ce0-114">-AsJob</span></span>
<span data-ttu-id="93ce0-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="93ce0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93ce0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ce0-116">-DefaultProfile</span></span>
<span data-ttu-id="93ce0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="93ce0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93ce0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93ce0-118">-InputObject</span></span>
<span data-ttu-id="93ce0-119">Obiekt przestrzeni nazw w usłudze Service Bus Migration Standard</span><span class="sxs-lookup"><span data-stu-id="93ce0-119">Service Bus Migration Standard Namespace Object</span></span>

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

### <span data-ttu-id="93ce0-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="93ce0-120">-Name</span></span>
<span data-ttu-id="93ce0-121">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="93ce0-121">Standard Namespace Name</span></span>

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

### <span data-ttu-id="93ce0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93ce0-122">-PassThru</span></span>
<span data-ttu-id="93ce0-123">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="93ce0-123">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="93ce0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93ce0-124">-ResourceGroupName</span></span>
<span data-ttu-id="93ce0-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="93ce0-125">Resource Group Name</span></span>

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

### <span data-ttu-id="93ce0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93ce0-126">-ResourceId</span></span>
<span data-ttu-id="93ce0-127">Identyfikator zasobu standardowej przestrzeni nazw w usłudze Service Bus Migration</span><span class="sxs-lookup"><span data-stu-id="93ce0-127">Service Bus Migration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="93ce0-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93ce0-128">-Confirm</span></span>
<span data-ttu-id="93ce0-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="93ce0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ce0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ce0-130">-WhatIf</span></span>
<span data-ttu-id="93ce0-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93ce0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ce0-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="93ce0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ce0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ce0-133">CommonParameters</span></span>
<span data-ttu-id="93ce0-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ce0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ce0-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ce0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ce0-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93ce0-136">INPUTS</span></span>

### <span data-ttu-id="93ce0-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="93ce0-137">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="93ce0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="93ce0-138">System.String</span></span>

## <span data-ttu-id="93ce0-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93ce0-139">OUTPUTS</span></span>

### <span data-ttu-id="93ce0-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93ce0-140">System.Boolean</span></span>

## <span data-ttu-id="93ce0-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="93ce0-141">NOTES</span></span>

## <span data-ttu-id="93ce0-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93ce0-142">RELATED LINKS</span></span>
