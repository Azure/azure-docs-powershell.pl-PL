---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspace.md
ms.openlocfilehash: 06cbaf240214bb61fb6bceac2827b9ce04d956f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220925"
---
# <span data-ttu-id="5ba90-101">Get-AzPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="5ba90-101">Get-AzPowerBIWorkspace</span></span>

## <span data-ttu-id="5ba90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ba90-102">SYNOPSIS</span></span>
<span data-ttu-id="5ba90-103">Pobiera obszary robocze ze zbioru obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="5ba90-103">Gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="5ba90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ba90-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ba90-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ba90-105">DESCRIPTION</span></span>
<span data-ttu-id="5ba90-106">Polecenie cmdlet **Get-AzPowerBIWorkspace** pobiera obszary robocze ze zbioru obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="5ba90-106">The **Get-AzPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="5ba90-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ba90-107">EXAMPLES</span></span>

### <span data-ttu-id="5ba90-108">Przykład 1: pobieranie obszarów roboczych kolekcji obszarów roboczych</span><span class="sxs-lookup"><span data-stu-id="5ba90-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="5ba90-109">To polecenie umożliwia pobieranie obszarów roboczych należących do kolekcji obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ba90-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="5ba90-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ba90-110">PARAMETERS</span></span>

### <span data-ttu-id="5ba90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ba90-111">-DefaultProfile</span></span>
<span data-ttu-id="5ba90-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5ba90-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ba90-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ba90-113">-ResourceGroupName</span></span>
<span data-ttu-id="5ba90-114">Określa nazwę grupy zasobów, do której należy kolekcja obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="5ba90-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="5ba90-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="5ba90-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="5ba90-116">Określa nazwę kolekcji obszarów roboczych, dla której ten aplet polecenia pobiera obszary robocze.</span><span class="sxs-lookup"><span data-stu-id="5ba90-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="5ba90-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ba90-117">CommonParameters</span></span>
<span data-ttu-id="5ba90-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ba90-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ba90-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ba90-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ba90-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ba90-120">INPUTS</span></span>

### <span data-ttu-id="5ba90-121">System. String</span><span class="sxs-lookup"><span data-stu-id="5ba90-121">System.String</span></span>

## <span data-ttu-id="5ba90-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ba90-122">OUTPUTS</span></span>

### <span data-ttu-id="5ba90-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5ba90-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="5ba90-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ba90-124">NOTES</span></span>

## <span data-ttu-id="5ba90-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ba90-125">RELATED LINKS</span></span>

[<span data-ttu-id="5ba90-126">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="5ba90-126">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)


