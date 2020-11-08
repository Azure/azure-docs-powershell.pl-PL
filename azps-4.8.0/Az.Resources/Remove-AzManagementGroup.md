---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroup.md
ms.openlocfilehash: ce2ccd21d7adecdf9602d29837295ad2ca65c952
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223641"
---
# <span data-ttu-id="8e01f-101">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8e01f-101">Remove-AzManagementGroup</span></span>

## <span data-ttu-id="8e01f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e01f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e01f-103">Usuwa grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="8e01f-103">Removes a Management Group</span></span>

## <span data-ttu-id="8e01f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e01f-104">SYNTAX</span></span>

### <span data-ttu-id="8e01f-105">GroupOperations (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8e01f-105">GroupOperations (Default)</span></span>
```
Remove-AzManagementGroup [-GroupName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e01f-106">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="8e01f-106">ManagementGroupObject</span></span>
```
Remove-AzManagementGroup -InputObject <PSManagementGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e01f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8e01f-107">DESCRIPTION</span></span>
<span data-ttu-id="8e01f-108">Polecenie cmdlet **Remove-AzManagementGroup** umożliwia usunięcie grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="8e01f-108">The **Remove-AzManagementGroup** cmdlet deletes a Management Group.</span></span>

## <span data-ttu-id="8e01f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e01f-109">EXAMPLES</span></span>

### <span data-ttu-id="8e01f-110">Przykład 1. Usuń grupę zarządzania</span><span class="sxs-lookup"><span data-stu-id="8e01f-110">Example 1: Remove a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroup -GroupName "TestGroup"
```

### <span data-ttu-id="8e01f-111">Przykład 2: Usuwanie grupy zarządzania przez obiekt połączeń rurowych PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8e01f-111">Example 2: Remove a Management Group by piping PSManagementGroup Object</span></span>
```powershell
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Remove-AzManagementGroup
```

## <span data-ttu-id="8e01f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e01f-112">PARAMETERS</span></span>

### <span data-ttu-id="8e01f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e01f-113">-DefaultProfile</span></span>
<span data-ttu-id="8e01f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e01f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e01f-115">-GroupName</span><span class="sxs-lookup"><span data-stu-id="8e01f-115">-GroupName</span></span>
<span data-ttu-id="8e01f-116">Identyfikator grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="8e01f-116">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e01f-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8e01f-117">-InputObject</span></span>
<span data-ttu-id="8e01f-118">Obiekt wejściowy z rozmowy Get</span><span class="sxs-lookup"><span data-stu-id="8e01f-118">Input Object from the Get call</span></span>

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

### <span data-ttu-id="8e01f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e01f-119">-PassThru</span></span>
<span data-ttu-id="8e01f-120">Powrót `true` po udanym wykonaniu</span><span class="sxs-lookup"><span data-stu-id="8e01f-120">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="8e01f-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e01f-121">-Confirm</span></span>
<span data-ttu-id="8e01f-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e01f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e01f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e01f-123">-WhatIf</span></span>
<span data-ttu-id="8e01f-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e01f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e01f-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e01f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e01f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e01f-126">CommonParameters</span></span>
<span data-ttu-id="8e01f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e01f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e01f-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e01f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e01f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e01f-129">INPUTS</span></span>

### <span data-ttu-id="8e01f-130">Microsoft. Azure. polecenia. resources. models. ManagementGroups. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="8e01f-130">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="8e01f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e01f-131">OUTPUTS</span></span>

### <span data-ttu-id="8e01f-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e01f-132">System.Boolean</span></span>

## <span data-ttu-id="8e01f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e01f-133">NOTES</span></span>

## <span data-ttu-id="8e01f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e01f-134">RELATED LINKS</span></span>
