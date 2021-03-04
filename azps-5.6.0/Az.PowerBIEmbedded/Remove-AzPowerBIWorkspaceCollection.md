---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 1623b706a3878b517680782462e07ebacce2daf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953441"
---
# <span data-ttu-id="a40f6-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a40f6-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="a40f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a40f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a40f6-103">Usuwa kolekcję obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="a40f6-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="a40f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a40f6-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a40f6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a40f6-105">DESCRIPTION</span></span>
<span data-ttu-id="a40f6-106">Polecenie **cmdlet Remove-AzPowerBIWorkspaceCollection** usuwa kolekcję obszarów roboczych usługi Power BI z subskrypcji platformy Azure i grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a40f6-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="a40f6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a40f6-107">EXAMPLES</span></span>

### <span data-ttu-id="a40f6-108">Przykład 1. Usuwanie kolekcji obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="a40f6-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="a40f6-109">To polecenie usuwa zbiór obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a40f6-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="a40f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a40f6-110">PARAMETERS</span></span>

### <span data-ttu-id="a40f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40f6-111">-DefaultProfile</span></span>
<span data-ttu-id="a40f6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a40f6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a40f6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a40f6-113">-ResourceGroupName</span></span>
<span data-ttu-id="a40f6-114">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa kolekcję obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="a40f6-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f6-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="a40f6-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="a40f6-116">Określa nazwę zbioru obszarów roboczych usługi Power BI, które usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a40f6-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a40f6-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a40f6-117">-Confirm</span></span>
<span data-ttu-id="a40f6-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a40f6-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40f6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a40f6-119">-WhatIf</span></span>
<span data-ttu-id="a40f6-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a40f6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a40f6-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a40f6-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40f6-122">CommonParameters</span></span>
<span data-ttu-id="a40f6-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40f6-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40f6-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40f6-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a40f6-125">INPUTS</span></span>

### <span data-ttu-id="a40f6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a40f6-126">System.String</span></span>

## <span data-ttu-id="a40f6-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a40f6-127">OUTPUTS</span></span>

### <span data-ttu-id="a40f6-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="a40f6-128">System.Void</span></span>

## <span data-ttu-id="a40f6-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a40f6-129">NOTES</span></span>

## <span data-ttu-id="a40f6-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a40f6-130">RELATED LINKS</span></span>

[<span data-ttu-id="a40f6-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a40f6-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="a40f6-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a40f6-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


