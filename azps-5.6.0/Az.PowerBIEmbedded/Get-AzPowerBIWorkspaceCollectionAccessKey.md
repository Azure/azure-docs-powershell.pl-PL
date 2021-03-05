---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: 06e17c012f52883d5e160698bb6f858f4644af6a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974609"
---
# <span data-ttu-id="465a5-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="465a5-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="465a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="465a5-102">SYNOPSIS</span></span>
<span data-ttu-id="465a5-103">Pobiera bieżące klucze dostępu skojarzone ze zbiorem obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="465a5-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="465a5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="465a5-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="465a5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="465a5-105">DESCRIPTION</span></span>
<span data-ttu-id="465a5-106">Polecenie **cmdlet Get-AzPowerBIWorkspaceCollectionAccessKey** pobiera bieżące klucze dostępu skojarzone ze zbiorem obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="465a5-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="465a5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="465a5-107">EXAMPLES</span></span>

### <span data-ttu-id="465a5-108">Przykład 1. Uzyskiwanie klawiszy dostępu</span><span class="sxs-lookup"><span data-stu-id="465a5-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="465a5-109">To polecenie pobiera klucze dostępu dla zbioru obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="465a5-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="465a5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="465a5-110">PARAMETERS</span></span>

### <span data-ttu-id="465a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="465a5-111">-DefaultProfile</span></span>
<span data-ttu-id="465a5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="465a5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="465a5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="465a5-113">-ResourceGroupName</span></span>
<span data-ttu-id="465a5-114">Określa nazwę grupy zasobów kolekcji.</span><span class="sxs-lookup"><span data-stu-id="465a5-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="465a5-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="465a5-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="465a5-116">Określa nazwę kolekcji obszarów roboczych usługi Power BI, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="465a5-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="465a5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="465a5-117">CommonParameters</span></span>
<span data-ttu-id="465a5-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="465a5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="465a5-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="465a5-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="465a5-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="465a5-120">INPUTS</span></span>

### <span data-ttu-id="465a5-121">System.String</span><span class="sxs-lookup"><span data-stu-id="465a5-121">System.String</span></span>

## <span data-ttu-id="465a5-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="465a5-122">OUTPUTS</span></span>

### <span data-ttu-id="465a5-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="465a5-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="465a5-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="465a5-124">NOTES</span></span>

## <span data-ttu-id="465a5-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="465a5-125">RELATED LINKS</span></span>

[<span data-ttu-id="465a5-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="465a5-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


