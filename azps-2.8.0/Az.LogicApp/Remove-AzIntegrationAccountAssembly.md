---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: ce3a3ae24a1064e036bc66e0fa7bfdaa6c74e0c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705000"
---
# <span data-ttu-id="02416-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="02416-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="02416-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02416-102">SYNOPSIS</span></span>
<span data-ttu-id="02416-103">Umożliwia usunięcie zestawu konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="02416-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="02416-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02416-104">SYNTAX</span></span>

### <span data-ttu-id="02416-105">ByIntegrationAccount (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02416-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02416-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="02416-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02416-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="02416-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02416-108">Opis</span><span class="sxs-lookup"><span data-stu-id="02416-108">DESCRIPTION</span></span>
<span data-ttu-id="02416-109">Polecenie cmdlet **Remove-AzIntegrationAccountAssembly** umożliwia usunięcie zestawu z konta integracji.</span><span class="sxs-lookup"><span data-stu-id="02416-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="02416-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02416-110">EXAMPLES</span></span>

### <span data-ttu-id="02416-111">Przykład 1. Usuwanie zestawu według parametrów</span><span class="sxs-lookup"><span data-stu-id="02416-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="02416-112">Usuwa zestaw o nazwie "sampleAssembly", który znajduje się na koncie integracji "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="02416-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="02416-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02416-113">PARAMETERS</span></span>

### <span data-ttu-id="02416-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02416-114">-DefaultProfile</span></span>
<span data-ttu-id="02416-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02416-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02416-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="02416-116">-InputObject</span></span>
<span data-ttu-id="02416-117">Zestaw kont integracyjnych.</span><span class="sxs-lookup"><span data-stu-id="02416-117">An integration account assembly.</span></span>

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

### <span data-ttu-id="02416-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02416-118">-Name</span></span>
<span data-ttu-id="02416-119">Nazwa zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="02416-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="02416-120">-Element nadrzędnyname</span><span class="sxs-lookup"><span data-stu-id="02416-120">-ParentName</span></span>
<span data-ttu-id="02416-121">Nazwa konta integracji.</span><span class="sxs-lookup"><span data-stu-id="02416-121">The integration account name.</span></span>

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

### <span data-ttu-id="02416-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02416-122">-PassThru</span></span>
<span data-ttu-id="02416-123">Zwraca, czy polecenie zostało wykonane prawidłowo, czy nie.</span><span class="sxs-lookup"><span data-stu-id="02416-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="02416-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02416-124">-ResourceGroupName</span></span>
<span data-ttu-id="02416-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="02416-125">The resource group name.</span></span>

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

### <span data-ttu-id="02416-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02416-126">-ResourceId</span></span>
<span data-ttu-id="02416-127">Identyfikator zasobu zestawu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="02416-127">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="02416-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02416-128">-Confirm</span></span>
<span data-ttu-id="02416-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02416-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02416-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02416-130">-WhatIf</span></span>
<span data-ttu-id="02416-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02416-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02416-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02416-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02416-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02416-133">CommonParameters</span></span>
<span data-ttu-id="02416-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02416-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02416-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02416-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02416-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02416-136">INPUTS</span></span>

### <span data-ttu-id="02416-137">Microsoft. Azure. Commands. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="02416-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="02416-138">System. String</span><span class="sxs-lookup"><span data-stu-id="02416-138">System.String</span></span>

## <span data-ttu-id="02416-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02416-139">OUTPUTS</span></span>

### <span data-ttu-id="02416-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02416-140">System.Boolean</span></span>

## <span data-ttu-id="02416-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02416-141">NOTES</span></span>

## <span data-ttu-id="02416-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02416-142">RELATED LINKS</span></span>
