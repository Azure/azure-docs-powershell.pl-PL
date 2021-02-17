---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178594"
---
# <span data-ttu-id="548a3-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="548a3-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="548a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="548a3-102">SYNOPSIS</span></span>
<span data-ttu-id="548a3-103">Polecenia cmdlet ustawiają migrację z przestrzeni nazw Standard do premium jako ciągi pełnych i parametry połączenia standardowej przestrzeni nazw wskazują teraz przestrzeń nazw Premium</span><span class="sxs-lookup"><span data-stu-id="548a3-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="548a3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="548a3-104">SYNTAX</span></span>

### <span data-ttu-id="548a3-105">MigrationConfigurationPropertiesSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="548a3-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="548a3-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="548a3-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="548a3-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="548a3-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548a3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="548a3-108">DESCRIPTION</span></span>
<span data-ttu-id="548a3-109">Polecenia cmdlet **Complete-AzServiceBusMigration** ustawiają migrację ze standardowej do premium przestrzeni nazw jako ciągi pełnych i parametry połączenia standardowej przestrzeni nazw wskazują teraz przestrzeń nazw Premium</span><span class="sxs-lookup"><span data-stu-id="548a3-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="548a3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="548a3-110">EXAMPLES</span></span>

### <span data-ttu-id="548a3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="548a3-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="548a3-112">Ustawia ukończoną migrację przestrzeni nazw "NamespaceStandardMigration".</span><span class="sxs-lookup"><span data-stu-id="548a3-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="548a3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="548a3-113">PARAMETERS</span></span>

### <span data-ttu-id="548a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548a3-114">-DefaultProfile</span></span>
<span data-ttu-id="548a3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="548a3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="548a3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="548a3-116">-InputObject</span></span>
<span data-ttu-id="548a3-117">Konfiguracja migracji autobusu usług — obiekt standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="548a3-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="548a3-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="548a3-118">-Name</span></span>
<span data-ttu-id="548a3-119">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="548a3-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="548a3-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="548a3-120">-PassThru</span></span>
<span data-ttu-id="548a3-121">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="548a3-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="548a3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548a3-122">-ResourceGroupName</span></span>
<span data-ttu-id="548a3-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="548a3-123">Resource Group Name</span></span>

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

### <span data-ttu-id="548a3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="548a3-124">-ResourceId</span></span>
<span data-ttu-id="548a3-125">Migracja autobusu usług — identyfikator zasobu standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="548a3-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="548a3-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="548a3-126">-Confirm</span></span>
<span data-ttu-id="548a3-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="548a3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="548a3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548a3-128">-WhatIf</span></span>
<span data-ttu-id="548a3-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="548a3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548a3-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="548a3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="548a3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548a3-131">CommonParameters</span></span>
<span data-ttu-id="548a3-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548a3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548a3-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="548a3-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548a3-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="548a3-134">INPUTS</span></span>

### <span data-ttu-id="548a3-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="548a3-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="548a3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="548a3-136">System.String</span></span>

## <span data-ttu-id="548a3-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="548a3-137">OUTPUTS</span></span>

### <span data-ttu-id="548a3-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="548a3-138">System.Boolean</span></span>

## <span data-ttu-id="548a3-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="548a3-139">NOTES</span></span>

## <span data-ttu-id="548a3-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="548a3-140">RELATED LINKS</span></span>
