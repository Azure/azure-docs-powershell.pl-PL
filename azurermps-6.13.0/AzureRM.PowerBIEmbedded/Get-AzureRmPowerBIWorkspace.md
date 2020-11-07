---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: 2217a6940e5f740c2499e95ff05f67c7144cbc3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716769"
---
# <span data-ttu-id="14c8f-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="14c8f-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="14c8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="14c8f-103">Pobiera obszary robocze ze zbioru obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="14c8f-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14c8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14c8f-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14c8f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="14c8f-105">DESCRIPTION</span></span>
<span data-ttu-id="14c8f-106">Polecenie cmdlet **Get-AzureRmPowerBIWorkspace** pobiera obszary robocze ze zbioru obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="14c8f-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="14c8f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14c8f-107">EXAMPLES</span></span>

### <span data-ttu-id="14c8f-108">Przykład 1: pobieranie obszarów roboczych kolekcji obszarów roboczych</span><span class="sxs-lookup"><span data-stu-id="14c8f-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="14c8f-109">To polecenie umożliwia pobieranie obszarów roboczych należących do kolekcji obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="14c8f-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="14c8f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14c8f-110">PARAMETERS</span></span>

### <span data-ttu-id="14c8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c8f-111">-DefaultProfile</span></span>
<span data-ttu-id="14c8f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="14c8f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14c8f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14c8f-113">-ResourceGroupName</span></span>
<span data-ttu-id="14c8f-114">Określa nazwę grupy zasobów, do której należy kolekcja obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="14c8f-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

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

### <span data-ttu-id="14c8f-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="14c8f-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="14c8f-116">Określa nazwę kolekcji obszarów roboczych, dla której ten aplet polecenia pobiera obszary robocze.</span><span class="sxs-lookup"><span data-stu-id="14c8f-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

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

### <span data-ttu-id="14c8f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c8f-117">CommonParameters</span></span>
<span data-ttu-id="14c8f-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14c8f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c8f-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c8f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c8f-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14c8f-120">INPUTS</span></span>

### <span data-ttu-id="14c8f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="14c8f-121">System.String</span></span>

## <span data-ttu-id="14c8f-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14c8f-122">OUTPUTS</span></span>

### <span data-ttu-id="14c8f-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="14c8f-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="14c8f-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14c8f-124">NOTES</span></span>

## <span data-ttu-id="14c8f-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14c8f-125">RELATED LINKS</span></span>

[<span data-ttu-id="14c8f-126">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="14c8f-126">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


