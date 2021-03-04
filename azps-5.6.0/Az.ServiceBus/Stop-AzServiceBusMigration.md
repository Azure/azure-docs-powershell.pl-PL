---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: fc0cc8acf45403593124135cab87072a719f291d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961601"
---
# <span data-ttu-id="e3d4e-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="e3d4e-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="e3d4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="e3d4e-103">{{Fill in the Synopsis}}</span><span class="sxs-lookup"><span data-stu-id="e3d4e-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="e3d4e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e3d4e-104">SYNTAX</span></span>

### <span data-ttu-id="e3d4e-105">MigrationConfigurationPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e3d4e-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3d4e-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e3d4e-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3d4e-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3d4e-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3d4e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e3d4e-108">DESCRIPTION</span></span>
<span data-ttu-id="e3d4e-109">Polecenie **cmdlet Stop-AzServiceBusMigration** kończy migrację między przestrzenią nazw Standard do premium</span><span class="sxs-lookup"><span data-stu-id="e3d4e-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="e3d4e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e3d4e-110">EXAMPLES</span></span>

### <span data-ttu-id="e3d4e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e3d4e-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="e3d4e-112">Polecenie cmdlet kończy migrację między standardową przestrzenią nazw a przestrzenią nazw Premium podaną podczas tworzenia konfiguracji migracji.</span><span class="sxs-lookup"><span data-stu-id="e3d4e-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="e3d4e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3d4e-113">PARAMETERS</span></span>

### <span data-ttu-id="e3d4e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3d4e-114">-DefaultProfile</span></span>
<span data-ttu-id="e3d4e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e3d4e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3d4e-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3d4e-116">-InputObject</span></span>
<span data-ttu-id="e3d4e-117">Obiekt przestrzeni nazw standardowej konfiguracji autobusu usług</span><span class="sxs-lookup"><span data-stu-id="e3d4e-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="e3d4e-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e3d4e-118">-Name</span></span>
<span data-ttu-id="e3d4e-119">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="e3d4e-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="e3d4e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3d4e-120">-PassThru</span></span>
<span data-ttu-id="e3d4e-121">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="e3d4e-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e3d4e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3d4e-122">-ResourceGroupName</span></span>
<span data-ttu-id="e3d4e-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e3d4e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e3d4e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3d4e-124">-ResourceId</span></span>
<span data-ttu-id="e3d4e-125">Identyfikator zasobu przestrzeni nazw standardowej konfiguracji autobusu usług</span><span class="sxs-lookup"><span data-stu-id="e3d4e-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="e3d4e-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3d4e-126">-Confirm</span></span>
<span data-ttu-id="e3d4e-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e3d4e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3d4e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3d4e-128">-WhatIf</span></span>
<span data-ttu-id="e3d4e-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3d4e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3d4e-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e3d4e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3d4e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3d4e-131">CommonParameters</span></span>
<span data-ttu-id="e3d4e-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3d4e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3d4e-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3d4e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3d4e-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3d4e-134">INPUTS</span></span>

### <span data-ttu-id="e3d4e-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="e3d4e-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="e3d4e-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e3d4e-136">System.String</span></span>

## <span data-ttu-id="e3d4e-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3d4e-137">OUTPUTS</span></span>

### <span data-ttu-id="e3d4e-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e3d4e-138">System.Boolean</span></span>

## <span data-ttu-id="e3d4e-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e3d4e-139">NOTES</span></span>

## <span data-ttu-id="e3d4e-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3d4e-140">RELATED LINKS</span></span>
