---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 9108f224297b23fd391e1a4c3afac4b826aa3dbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183954"
---
# <span data-ttu-id="e3fdf-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="e3fdf-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="e3fdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="e3fdf-103">Pobiera bieżące klucze dostępu skojarzone ze zbiorem obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="e3fdf-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="e3fdf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e3fdf-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3fdf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e3fdf-105">DESCRIPTION</span></span>
<span data-ttu-id="e3fdf-106">Polecenie **cmdlet Get-AzPowerBIWorkspaceCollectionAccessKey** pobiera bieżące klucze dostępu skojarzone ze zbiorem obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="e3fdf-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="e3fdf-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e3fdf-107">EXAMPLES</span></span>

### <span data-ttu-id="e3fdf-108">Przykład 1. Uzyskiwanie klawiszy dostępu</span><span class="sxs-lookup"><span data-stu-id="e3fdf-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="e3fdf-109">To polecenie pobiera klucze dostępu dla zbioru obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="e3fdf-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="e3fdf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3fdf-110">PARAMETERS</span></span>

### <span data-ttu-id="e3fdf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3fdf-111">-DefaultProfile</span></span>
<span data-ttu-id="e3fdf-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e3fdf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3fdf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3fdf-113">-ResourceGroupName</span></span>
<span data-ttu-id="e3fdf-114">Określa nazwę grupy zasobów kolekcji.</span><span class="sxs-lookup"><span data-stu-id="e3fdf-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="e3fdf-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="e3fdf-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="e3fdf-116">Określa nazwę kolekcji obszarów roboczych usługi Power BI, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3fdf-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e3fdf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3fdf-117">CommonParameters</span></span>
<span data-ttu-id="e3fdf-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3fdf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3fdf-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3fdf-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3fdf-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3fdf-120">INPUTS</span></span>

### <span data-ttu-id="e3fdf-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e3fdf-121">System.String</span></span>

## <span data-ttu-id="e3fdf-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3fdf-122">OUTPUTS</span></span>

### <span data-ttu-id="e3fdf-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="e3fdf-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="e3fdf-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e3fdf-124">NOTES</span></span>

## <span data-ttu-id="e3fdf-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3fdf-125">RELATED LINKS</span></span>

[<span data-ttu-id="e3fdf-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="e3fdf-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


