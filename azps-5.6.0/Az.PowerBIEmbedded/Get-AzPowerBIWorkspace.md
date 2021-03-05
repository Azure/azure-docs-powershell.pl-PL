---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: d9c93bc487817d99b217519453dea10543852a1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974618"
---
# <span data-ttu-id="c49c3-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="c49c3-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="c49c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c49c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c49c3-103">Pobiera obszary robocze w zbiorze obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="c49c3-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="c49c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c49c3-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c49c3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c49c3-105">DESCRIPTION</span></span>
<span data-ttu-id="c49c3-106">Polecenie **cmdlet Get-AzPowerBIWorkspace** pobiera obszary robocze w kolekcji obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="c49c3-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="c49c3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c49c3-107">EXAMPLES</span></span>

### <span data-ttu-id="c49c3-108">Przykład 1. Uzyskiwanie obszarów roboczych zbioru obszarów roboczych</span><span class="sxs-lookup"><span data-stu-id="c49c3-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="c49c3-109">To polecenie pobiera obszary robocze należące do zbioru obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="c49c3-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="c49c3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c49c3-110">PARAMETERS</span></span>

### <span data-ttu-id="c49c3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c49c3-111">-DefaultProfile</span></span>
<span data-ttu-id="c49c3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c49c3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c49c3-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c49c3-113">-ResourceGroupName</span></span>
<span data-ttu-id="c49c3-114">Określa nazwę grupy zasobów, do której należy kolekcja obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="c49c3-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="c49c3-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="c49c3-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="c49c3-116">Określa nazwę kolekcji obszarów roboczych, dla której to polecenie cmdlet otrzymuje obszary robocze.</span><span class="sxs-lookup"><span data-stu-id="c49c3-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="c49c3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49c3-117">CommonParameters</span></span>
<span data-ttu-id="c49c3-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c49c3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49c3-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c49c3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49c3-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c49c3-120">INPUTS</span></span>

### <span data-ttu-id="c49c3-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c49c3-121">System.String</span></span>

## <span data-ttu-id="c49c3-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c49c3-122">OUTPUTS</span></span>

### <span data-ttu-id="c49c3-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c49c3-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="c49c3-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c49c3-124">NOTES</span></span>

## <span data-ttu-id="c49c3-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c49c3-125">RELATED LINKS</span></span>

[<span data-ttu-id="c49c3-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="c49c3-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


