---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220786"
---
# <span data-ttu-id="bd73b-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bd73b-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="bd73b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd73b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd73b-103">Umożliwia usunięcie zestawu konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="bd73b-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="bd73b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd73b-104">SYNTAX</span></span>

### <span data-ttu-id="bd73b-105">ByIntegrationAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bd73b-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd73b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bd73b-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd73b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bd73b-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd73b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bd73b-108">DESCRIPTION</span></span>
<span data-ttu-id="bd73b-109">Polecenie cmdlet **Remove-AzIntegrationAccountAssembly** umożliwia usunięcie zestawu z konta integracji.</span><span class="sxs-lookup"><span data-stu-id="bd73b-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="bd73b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd73b-110">EXAMPLES</span></span>

### <span data-ttu-id="bd73b-111">Przykład 1. Usuwanie zestawu według parametrów</span><span class="sxs-lookup"><span data-stu-id="bd73b-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="bd73b-112">Usuwa zestaw o nazwie "sampleAssembly", który znajduje się na koncie integracji "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="bd73b-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="bd73b-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd73b-113">PARAMETERS</span></span>

### <span data-ttu-id="bd73b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd73b-114">-DefaultProfile</span></span>
<span data-ttu-id="bd73b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd73b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd73b-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bd73b-116">-InputObject</span></span>
<span data-ttu-id="bd73b-117">Zestaw kont integracyjnych.</span><span class="sxs-lookup"><span data-stu-id="bd73b-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd73b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd73b-118">-Name</span></span>
<span data-ttu-id="bd73b-119">Nazwa zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="bd73b-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd73b-120">-Element nadrzędnyname</span><span class="sxs-lookup"><span data-stu-id="bd73b-120">-ParentName</span></span>
<span data-ttu-id="bd73b-121">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="bd73b-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd73b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd73b-122">-PassThru</span></span>
<span data-ttu-id="bd73b-123">Zwraca, czy polecenie zostało wykonane prawidłowo, czy nie.</span><span class="sxs-lookup"><span data-stu-id="bd73b-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="bd73b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd73b-124">-ResourceGroupName</span></span>
<span data-ttu-id="bd73b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd73b-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd73b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd73b-126">-ResourceId</span></span>
<span data-ttu-id="bd73b-127">Identyfikator zasobu zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="bd73b-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd73b-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd73b-128">-Confirm</span></span>
<span data-ttu-id="bd73b-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd73b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd73b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd73b-130">-WhatIf</span></span>
<span data-ttu-id="bd73b-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd73b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd73b-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd73b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd73b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd73b-133">CommonParameters</span></span>
<span data-ttu-id="bd73b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd73b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd73b-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd73b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd73b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd73b-136">INPUTS</span></span>

### <span data-ttu-id="bd73b-137">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="bd73b-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="bd73b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bd73b-138">System.String</span></span>

## <span data-ttu-id="bd73b-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd73b-139">OUTPUTS</span></span>

### <span data-ttu-id="bd73b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd73b-140">System.Boolean</span></span>

## <span data-ttu-id="bd73b-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd73b-141">NOTES</span></span>

## <span data-ttu-id="bd73b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd73b-142">RELATED LINKS</span></span>
