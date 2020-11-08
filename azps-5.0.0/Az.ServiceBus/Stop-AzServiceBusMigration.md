---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/stop-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Stop-AzServiceBusMigration.md
ms.openlocfilehash: 615a09d735867d45f9db75ce229d39bc8d9bf75b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225144"
---
# <span data-ttu-id="4fd11-101">Stop-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="4fd11-101">Stop-AzServiceBusMigration</span></span>

## <span data-ttu-id="4fd11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4fd11-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd11-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="4fd11-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="4fd11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4fd11-104">SYNTAX</span></span>

### <span data-ttu-id="4fd11-105">MigrationConfigurationPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4fd11-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Stop-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd11-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4fd11-106">NamespaceInputObjectSet</span></span>
```
Stop-AzServiceBusMigration [-InputObject] <PSServiceBusDRConfigurationAttributes> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fd11-107">NamespaceResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4fd11-107">NamespaceResourceIdParameterSet</span></span>
```
Stop-AzServiceBusMigration [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fd11-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4fd11-108">DESCRIPTION</span></span>
<span data-ttu-id="4fd11-109">Polecenia cmdlet **stop-AzServiceBusMigration** kończą migrację między standardowym obszarem nazw Premium</span><span class="sxs-lookup"><span data-stu-id="4fd11-109">The **Stop-AzServiceBusMigration** cmdlets terminates the Migration between Standard to premium namespace</span></span>

## <span data-ttu-id="4fd11-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4fd11-110">EXAMPLES</span></span>

### <span data-ttu-id="4fd11-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4fd11-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration
```

<span data-ttu-id="4fd11-112">Polecenie cmdlet powoduje zakończenie migracji między standardową przestrzenią nazw a obszarem nazw Premium podanym podczas tworzenia konfiguracji migracji.</span><span class="sxs-lookup"><span data-stu-id="4fd11-112">Cmdlet terminates the migration between Standard namespace and Premium namespace provided while creating the migration configuration.</span></span>

## <span data-ttu-id="4fd11-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4fd11-113">PARAMETERS</span></span>

### <span data-ttu-id="4fd11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd11-114">-DefaultProfile</span></span>
<span data-ttu-id="4fd11-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4fd11-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fd11-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4fd11-116">-InputObject</span></span>
<span data-ttu-id="4fd11-117">Obiekt Namespace konfiguracji migracji usługi Service Bus Standard</span><span class="sxs-lookup"><span data-stu-id="4fd11-117">Service Bus Migration Configuration Standard Namespace Object</span></span>

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

### <span data-ttu-id="4fd11-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4fd11-118">-Name</span></span>
<span data-ttu-id="4fd11-119">Nazwa standardowej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="4fd11-119">Standard Namespace Name</span></span>

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

### <span data-ttu-id="4fd11-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fd11-120">-PassThru</span></span>
<span data-ttu-id="4fd11-121">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="4fd11-121">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4fd11-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fd11-122">-ResourceGroupName</span></span>
<span data-ttu-id="4fd11-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4fd11-123">Resource Group Name</span></span>

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

### <span data-ttu-id="4fd11-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fd11-124">-ResourceId</span></span>
<span data-ttu-id="4fd11-125">Identyfikator zasobu standardowej przestrzeni nazw konfiguracji migracji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="4fd11-125">Service Bus Migration Configuration Standard Namespace Resource Id</span></span>

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

### <span data-ttu-id="4fd11-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4fd11-126">-Confirm</span></span>
<span data-ttu-id="4fd11-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fd11-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fd11-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fd11-128">-WhatIf</span></span>
<span data-ttu-id="4fd11-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fd11-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fd11-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4fd11-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fd11-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd11-131">CommonParameters</span></span>
<span data-ttu-id="4fd11-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd11-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd11-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd11-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd11-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4fd11-134">INPUTS</span></span>

### <span data-ttu-id="4fd11-135">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusDRConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="4fd11-135">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusDRConfigurationAttributes</span></span>

### <span data-ttu-id="4fd11-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4fd11-136">System.String</span></span>

## <span data-ttu-id="4fd11-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4fd11-137">OUTPUTS</span></span>

### <span data-ttu-id="4fd11-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4fd11-138">System.Boolean</span></span>

## <span data-ttu-id="4fd11-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4fd11-139">NOTES</span></span>

## <span data-ttu-id="4fd11-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4fd11-140">RELATED LINKS</span></span>
