---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesAccount.md
ms.openlocfilehash: 19f194d9402c2d5101b1da56c7c7a2a2208345aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968385"
---
# <span data-ttu-id="e5c84-101">Remove-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e5c84-101">Remove-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="e5c84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5c84-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c84-103">Usuwa konto usługi Azure NetApp Files (ANF).</span><span class="sxs-lookup"><span data-stu-id="e5c84-103">Deletes an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="e5c84-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e5c84-104">SYNTAX</span></span>

### <span data-ttu-id="e5c84-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e5c84-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c84-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5c84-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5c84-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5c84-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesAccount -InputObject <PSNetAppFilesAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5c84-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e5c84-108">DESCRIPTION</span></span>
<span data-ttu-id="e5c84-109">Polecenie **cmdlet Remove-AzNetAppFilesAccount** usuwa konto ANF.</span><span class="sxs-lookup"><span data-stu-id="e5c84-109">The **Remove-AzNetAppFilesAccount** cmdlet deletes an ANF account.</span></span>

## <span data-ttu-id="e5c84-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e5c84-110">EXAMPLES</span></span>

### <span data-ttu-id="e5c84-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e5c84-111">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"
```

<span data-ttu-id="e5c84-112">To polecenie usuwa konto ANF "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="e5c84-112">This command deletes the ANF account "MyAnfAccount".</span></span>

## <span data-ttu-id="e5c84-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5c84-113">PARAMETERS</span></span>

### <span data-ttu-id="e5c84-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5c84-114">-DefaultProfile</span></span>
<span data-ttu-id="e5c84-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5c84-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5c84-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5c84-116">-InputObject</span></span>
<span data-ttu-id="e5c84-117">Obiekt konta do usunięcia</span><span class="sxs-lookup"><span data-stu-id="e5c84-117">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c84-118">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e5c84-118">-Name</span></span>
<span data-ttu-id="e5c84-119">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="e5c84-119">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c84-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5c84-120">-PassThru</span></span>
<span data-ttu-id="e5c84-121">Zwracanie, czy określone konto zostało pomyślnie usunięte</span><span class="sxs-lookup"><span data-stu-id="e5c84-121">Return whether the specified account was successfully removed</span></span>

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

### <span data-ttu-id="e5c84-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c84-122">-ResourceGroupName</span></span>
<span data-ttu-id="e5c84-123">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="e5c84-123">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5c84-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5c84-124">-ResourceId</span></span>
<span data-ttu-id="e5c84-125">Identyfikator zasobu konta ANF</span><span class="sxs-lookup"><span data-stu-id="e5c84-125">The resource id of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c84-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e5c84-126">-Confirm</span></span>
<span data-ttu-id="e5c84-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e5c84-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5c84-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5c84-128">-WhatIf</span></span>
<span data-ttu-id="e5c84-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5c84-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5c84-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e5c84-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5c84-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5c84-131">CommonParameters</span></span>
<span data-ttu-id="e5c84-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5c84-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5c84-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5c84-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5c84-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5c84-134">INPUTS</span></span>

### <span data-ttu-id="e5c84-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e5c84-135">System.String</span></span>

### <span data-ttu-id="e5c84-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="e5c84-136">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="e5c84-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5c84-137">OUTPUTS</span></span>

### <span data-ttu-id="e5c84-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e5c84-138">System.Boolean</span></span>

## <span data-ttu-id="e5c84-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e5c84-139">NOTES</span></span>

## <span data-ttu-id="e5c84-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5c84-140">RELATED LINKS</span></span>
