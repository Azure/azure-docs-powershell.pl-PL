---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspace.md
ms.openlocfilehash: c94486e33ac39bff9d378840a6ab0ad041fa998e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527973"
---
# <span data-ttu-id="07936-101">Get-AzureRmPowerBIWorkspace</span><span class="sxs-lookup"><span data-stu-id="07936-101">Get-AzureRmPowerBIWorkspace</span></span>

## <span data-ttu-id="07936-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="07936-102">SYNOPSIS</span></span>
<span data-ttu-id="07936-103">Pobiera obszary robocze ze zbioru obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="07936-103">Gets the workspaces in a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07936-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="07936-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspace [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07936-105">Opis</span><span class="sxs-lookup"><span data-stu-id="07936-105">DESCRIPTION</span></span>
<span data-ttu-id="07936-106">Polecenie cmdlet **Get-AzureRmPowerBIWorkspace** pobiera obszary robocze ze zbioru obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="07936-106">The **Get-AzureRmPowerBIWorkspace** cmdlet gets the workspaces in a Power BI workspace collection.</span></span>

## <span data-ttu-id="07936-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="07936-107">EXAMPLES</span></span>

### <span data-ttu-id="07936-108">Przykład 1: pobieranie obszarów roboczych kolekcji obszarów roboczych</span><span class="sxs-lookup"><span data-stu-id="07936-108">Example 1: Get workspaces of a workspace collection</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspace -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="07936-109">To polecenie umożliwia pobieranie obszarów roboczych należących do kolekcji obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="07936-109">This command gets the workspaces that belong to the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="07936-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07936-110">PARAMETERS</span></span>

### <span data-ttu-id="07936-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07936-111">-DefaultProfile</span></span>
<span data-ttu-id="07936-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="07936-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07936-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07936-113">-ResourceGroupName</span></span>
<span data-ttu-id="07936-114">Określa nazwę grupy zasobów, do której należy kolekcja obszarów roboczych.</span><span class="sxs-lookup"><span data-stu-id="07936-114">Specifies the name of the resource group to which the workspace collection belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07936-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="07936-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="07936-116">Określa nazwę kolekcji obszarów roboczych, dla której ten aplet polecenia pobiera obszary robocze.</span><span class="sxs-lookup"><span data-stu-id="07936-116">Specifies the name of the workspace collection for which this cmdlet gets workspaces.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07936-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07936-117">CommonParameters</span></span>
<span data-ttu-id="07936-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07936-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07936-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07936-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07936-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07936-120">INPUTS</span></span>

### <span data-ttu-id="07936-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="07936-121">None</span></span>
<span data-ttu-id="07936-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="07936-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07936-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="07936-123">OUTPUTS</span></span>

### <span data-ttu-id="07936-124">Microsoft. Azure. Commands. Management. PowerBIEmbedded. models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="07936-124">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspace</span></span>

## <span data-ttu-id="07936-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="07936-125">NOTES</span></span>

## <span data-ttu-id="07936-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07936-126">RELATED LINKS</span></span>

[<span data-ttu-id="07936-127">Get-AzureRmPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="07936-127">Get-AzureRmPowerBIWorkspaceCollection</span></span>](./Get-AzureRmPowerBIWorkspaceCollection.md)


