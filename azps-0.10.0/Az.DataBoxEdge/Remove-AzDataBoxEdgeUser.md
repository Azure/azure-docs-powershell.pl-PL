---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 1d6c99a44e2163f2d441dcacc87cf202f334f330
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891566"
---
# <span data-ttu-id="70ee5-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="70ee5-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="70ee5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="70ee5-102">SYNOPSIS</span></span>
<span data-ttu-id="70ee5-103">Usuwa użytkownika na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="70ee5-103">Removes a user on a device.</span></span>

## <span data-ttu-id="70ee5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="70ee5-104">SYNTAX</span></span>

### <span data-ttu-id="70ee5-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="70ee5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ee5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="70ee5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70ee5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="70ee5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70ee5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="70ee5-108">DESCRIPTION</span></span>
<span data-ttu-id="70ee5-109">Polecenie cmdlet **Remove-AzDataBoxEdgeUser** usuwa użytkownika na urządzeniu z danymi na krawędziach pola danych.</span><span class="sxs-lookup"><span data-stu-id="70ee5-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="70ee5-110">Możliwość tworzenia tylko użytkowników typu `Share` jest obsługiwana.</span><span class="sxs-lookup"><span data-stu-id="70ee5-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="70ee5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="70ee5-111">EXAMPLES</span></span>

### <span data-ttu-id="70ee5-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="70ee5-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="70ee5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="70ee5-113">PARAMETERS</span></span>

### <span data-ttu-id="70ee5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70ee5-114">-AsJob</span></span>
<span data-ttu-id="70ee5-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="70ee5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="70ee5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70ee5-116">-DefaultProfile</span></span>
<span data-ttu-id="70ee5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="70ee5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70ee5-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="70ee5-118">-DeviceName</span></span>
<span data-ttu-id="70ee5-119">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="70ee5-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ee5-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="70ee5-120">-InputObject</span></span>
<span data-ttu-id="70ee5-121">Obiekt wejściowy</span><span class="sxs-lookup"><span data-stu-id="70ee5-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="70ee5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="70ee5-122">-Name</span></span>
<span data-ttu-id="70ee5-123">Nazwie</span><span class="sxs-lookup"><span data-stu-id="70ee5-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ee5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="70ee5-124">-PassThru</span></span>
<span data-ttu-id="70ee5-125">Zwraca wartość PRAWDA, jeśli powodzenie</span><span class="sxs-lookup"><span data-stu-id="70ee5-125">returns true if successful</span></span>

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

### <span data-ttu-id="70ee5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70ee5-126">-ResourceGroupName</span></span>
<span data-ttu-id="70ee5-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="70ee5-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70ee5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70ee5-128">-ResourceId</span></span>
<span data-ttu-id="70ee5-129">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="70ee5-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70ee5-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="70ee5-130">-Confirm</span></span>
<span data-ttu-id="70ee5-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70ee5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70ee5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70ee5-132">-WhatIf</span></span>
<span data-ttu-id="70ee5-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="70ee5-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70ee5-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="70ee5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70ee5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70ee5-135">CommonParameters</span></span>
<span data-ttu-id="70ee5-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70ee5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70ee5-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70ee5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70ee5-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="70ee5-138">INPUTS</span></span>

### <span data-ttu-id="70ee5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="70ee5-139">System.String</span></span>

### <span data-ttu-id="70ee5-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="70ee5-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="70ee5-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="70ee5-141">OUTPUTS</span></span>

### <span data-ttu-id="70ee5-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="70ee5-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="70ee5-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="70ee5-143">NOTES</span></span>

## <span data-ttu-id="70ee5-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="70ee5-144">RELATED LINKS</span></span>
