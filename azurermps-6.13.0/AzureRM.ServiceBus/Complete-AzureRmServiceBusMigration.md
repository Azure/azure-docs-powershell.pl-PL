---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/complete-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Complete-AzureRmServiceBusMigration.md
ms.openlocfilehash: 0006e4768dc27994d18e93e48696b5ee9a514c45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718269"
---
# <span data-ttu-id="9bf80-101">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="9bf80-101">Complete-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="9bf80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bf80-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf80-103">Polecenia cmdlet Ustaw migrację z obszaru nazw standardowy do Premium jako ukończone i parametry połączenia dla standardowej przestrzeni nazw wskazują obszar nazw Premium</span><span class="sxs-lookup"><span data-stu-id="9bf80-103">Cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bf80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bf80-104">SYNTAX</span></span>

### <span data-ttu-id="9bf80-105">MigrationConfigurationPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9bf80-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf80-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9bf80-106">NamespaceInputObjectSet</span></span>
```
Complete-AzureRmServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bf80-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bf80-107">NamespaceResourceIdParameterSet</span></span>
```
Complete-AzureRmServiceBusMigration [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bf80-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9bf80-108">DESCRIPTION</span></span>
<span data-ttu-id="9bf80-109">Polecenia cmdlet **Complete-AzureRmServiceBusMigration** umożliwiają ustawienie migracji z przestrzeni nazw Standard do Premium jako ukończone i parametry połączenia dla standardowej przestrzeni nazw wskazują na obszar nazw Premium.</span><span class="sxs-lookup"><span data-stu-id="9bf80-109">The **Complete-AzureRmServiceBusMigration** cmdlets set the Migration from Standard to premium namespace as complete and connection strings of standard namespace now point to Premium namespace</span></span>

## <span data-ttu-id="9bf80-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bf80-110">EXAMPLES</span></span>

### <span data-ttu-id="9bf80-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9bf80-111">Example 1</span></span>
```powershell
PS C:\> Complete-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name NamespaceStandardMirgation
```

<span data-ttu-id="9bf80-112">Ustawia migrację przestrzeni nazw "NamespaceStandardMirgation" jako ukończonej.</span><span class="sxs-lookup"><span data-stu-id="9bf80-112">Sets the Migration of 'NamespaceStandardMirgation' namespace as complete.</span></span>

## <span data-ttu-id="9bf80-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bf80-113">PARAMETERS</span></span>

### <span data-ttu-id="9bf80-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf80-114">-DefaultProfile</span></span>
<span data-ttu-id="9bf80-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf80-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bf80-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9bf80-116">-InputObject</span></span>
<span data-ttu-id="9bf80-117">Konfiguracja migracji magistrali usług — standardowy obiekt obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="9bf80-117">Service Bus Migration configuration - Standard Namespace Object</span></span>

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

### <span data-ttu-id="9bf80-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9bf80-118">-Name</span></span>
<span data-ttu-id="9bf80-119">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="9bf80-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="9bf80-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bf80-120">-PassThru</span></span>
<span data-ttu-id="9bf80-121">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="9bf80-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="9bf80-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bf80-122">-ResourceGroupName</span></span>
<span data-ttu-id="9bf80-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9bf80-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9bf80-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bf80-124">-ResourceId</span></span>
<span data-ttu-id="9bf80-125">Migratio magistrali usług — Identyfikator zasobu standardowego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="9bf80-125">Service Bus Migratio - Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="9bf80-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9bf80-126">-Confirm</span></span>
<span data-ttu-id="9bf80-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bf80-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bf80-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bf80-128">-WhatIf</span></span>
<span data-ttu-id="9bf80-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bf80-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bf80-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9bf80-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bf80-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf80-131">CommonParameters</span></span>
<span data-ttu-id="9bf80-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf80-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf80-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bf80-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf80-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bf80-134">INPUTS</span></span>

### <span data-ttu-id="9bf80-135">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="9bf80-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>
<span data-ttu-id="9bf80-136">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9bf80-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="9bf80-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf80-137">System.String</span></span>

## <span data-ttu-id="9bf80-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bf80-138">OUTPUTS</span></span>

### <span data-ttu-id="9bf80-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9bf80-139">System.Boolean</span></span>

## <span data-ttu-id="9bf80-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bf80-140">NOTES</span></span>

## <span data-ttu-id="9bf80-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bf80-141">RELATED LINKS</span></span>
