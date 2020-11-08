---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/complete-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Complete-AzServiceBusMigration.md
ms.openlocfilehash: 883ecf9337cea2b46166b4c1be8625c9763eb7db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233613"
---
# <span data-ttu-id="41a3c-101">Complete-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="41a3c-101">Complete-AzServiceBusMigration</span></span>

## <span data-ttu-id="41a3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="41a3c-103">Polecenia cmdlet Ustaw migrację z obszaru nazw standardowy do Premium jako ukończone i parametry połączenia dla standardowej przestrzeni nazw wskazują obszar nazw Premium</span><span class="sxs-lookup"><span data-stu-id="41a3c-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="41a3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41a3c-104">SYNTAX</span></span>

### <span data-ttu-id="41a3c-105">MigrationConfigurationPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="41a3c-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41a3c-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="41a3c-106">NamespaceInputObjectSet</span></span>
```
Complete-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41a3c-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="41a3c-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41a3c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="41a3c-108">DESCRIPTION</span></span>
<span data-ttu-id="41a3c-109">Polecenia cmdlet **Complete-AzServiceBusMigration** umożliwiają ustawienie migracji z przestrzeni nazw Standard do Premium jako ukończone i parametry połączenia dla standardowej przestrzeni nazw wskazują na obszar nazw Premium.</span><span class="sxs-lookup"><span data-stu-id="41a3c-109">The **Complete-AzServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="41a3c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41a3c-110">EXAMPLES</span></span>

### <span data-ttu-id="41a3c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41a3c-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMigration
```

<span data-ttu-id="41a3c-112">Ustawia migrację przestrzeni nazw "NamespaceStandardMigration" jako ukończonej.</span><span class="sxs-lookup"><span data-stu-id="41a3c-112">Sets the Migration of 'NamespaceStandardMigration' namespace as complete.</span></span>

## <span data-ttu-id="41a3c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41a3c-113">PARAMETERS</span></span>

### <span data-ttu-id="41a3c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41a3c-114">-DefaultProfile</span></span>
<span data-ttu-id="41a3c-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41a3c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41a3c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="41a3c-116">-InputObject</span></span>
<span data-ttu-id="41a3c-117">Konfiguracja migracji magistrali usług — standardowy obiekt obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="41a3c-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="41a3c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41a3c-118">-Name</span></span>
<span data-ttu-id="41a3c-119">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="41a3c-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="41a3c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41a3c-120">-PassThru</span></span>
<span data-ttu-id="41a3c-121">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="41a3c-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="41a3c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41a3c-122">-ResourceGroupName</span></span>
<span data-ttu-id="41a3c-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="41a3c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="41a3c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41a3c-124">-ResourceId</span></span>
<span data-ttu-id="41a3c-125">Migracja magistrali usług — Identyfikator zasobu standardowego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="41a3c-125">Service Bus Migration - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="41a3c-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41a3c-126">-Confirm</span></span>
<span data-ttu-id="41a3c-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41a3c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41a3c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41a3c-128">-WhatIf</span></span>
<span data-ttu-id="41a3c-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41a3c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41a3c-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41a3c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41a3c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a3c-131">CommonParameters</span></span>
<span data-ttu-id="41a3c-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41a3c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a3c-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41a3c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a3c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41a3c-134">INPUTS</span></span>

### <span data-ttu-id="41a3c-135">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="41a3c-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="41a3c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="41a3c-136">System.String</span></span>

## <span data-ttu-id="41a3c-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41a3c-137">OUTPUTS</span></span>

### <span data-ttu-id="41a3c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41a3c-138">System.Boolean</span></span>

## <span data-ttu-id="41a3c-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41a3c-139">NOTES</span></span>

## <span data-ttu-id="41a3c-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41a3c-140">RELATED LINKS</span></span>
