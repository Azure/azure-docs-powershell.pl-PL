---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: cbc6be671669b3db8af41c0e5de4333b811e271a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708310"
---
# <span data-ttu-id="db063-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="db063-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="db063-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db063-102">SYNOPSIS</span></span>
<span data-ttu-id="db063-103">Usuwa grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="db063-103">Removes a Management Group</span></span>

## <span data-ttu-id="db063-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db063-104">SYNTAX</span></span>

### <span data-ttu-id="db063-105">GroupOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="db063-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db063-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="db063-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db063-107">Opis</span><span class="sxs-lookup"><span data-stu-id="db063-107">DESCRIPTION</span></span>
<span data-ttu-id="db063-108">Polecenie cmdlet **Remove-AzManagementGroup** umożliwia usunięcie grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="db063-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="db063-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db063-109">EXAMPLES</span></span>

### <span data-ttu-id="db063-110">Przykład 1 — Usuwanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="db063-110">Example 1 - Remove a Management Group</span></span>
```
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="db063-111">Przykład 2 — Usuwanie grupy zarządzania za pomocą obiektu PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="db063-111">Example 2 - Remove a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-Remove-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="db063-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db063-112">PARAMETERS</span></span>

### <span data-ttu-id="db063-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db063-113">-DefaultProfile</span></span>
<span data-ttu-id="db063-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db063-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db063-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="db063-115">-GroupName</span></span>
<span data-ttu-id="db063-116">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="db063-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db063-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="db063-117">-InputObject</span></span>
<span data-ttu-id="db063-118">Obiekt wejściowy z rozmowy Get</span><span class="sxs-lookup"><span data-stu-id="db063-118">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db063-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db063-119">-PassThru</span></span>
<span data-ttu-id="db063-120">Powrót `true` po udanym wykonaniu</span><span class="sxs-lookup"><span data-stu-id="db063-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="db063-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="db063-121">-Confirm</span></span>
<span data-ttu-id="db063-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db063-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db063-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db063-123">-WhatIf</span></span>
<span data-ttu-id="db063-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db063-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db063-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="db063-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db063-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db063-126">CommonParameters</span></span>
<span data-ttu-id="db063-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db063-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db063-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db063-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db063-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db063-129">INPUTS</span></span>

### <span data-ttu-id="db063-130">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="db063-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="db063-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db063-131">OUTPUTS</span></span>

### <span data-ttu-id="db063-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db063-132">System.Boolean</span></span>

## <span data-ttu-id="db063-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db063-133">NOTES</span></span>

## <span data-ttu-id="db063-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db063-134">RELATED LINKS</span></span>
