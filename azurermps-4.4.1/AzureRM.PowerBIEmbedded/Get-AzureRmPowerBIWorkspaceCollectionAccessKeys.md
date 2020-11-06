---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 387edc5f2a2fb02fb035b2090aade015573cf6d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553184"
---
# <span data-ttu-id="926cc-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="926cc-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="926cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="926cc-102">SYNOPSIS</span></span>
<span data-ttu-id="926cc-103">Pobiera bieżące klucze dostępu skojarzone z kolekcją obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="926cc-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="926cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="926cc-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="926cc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="926cc-105">DESCRIPTION</span></span>
<span data-ttu-id="926cc-106">Polecenie cmdlet **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** pobiera bieżące klucze dostępu skojarzone z kolekcją obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="926cc-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="926cc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="926cc-107">EXAMPLES</span></span>

### <span data-ttu-id="926cc-108">Przykład 1: uzyskiwanie klawiszy dostępu</span><span class="sxs-lookup"><span data-stu-id="926cc-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="926cc-109">To polecenie pobiera klucze programu Access dla kolekcji obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="926cc-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="926cc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="926cc-110">PARAMETERS</span></span>

### <span data-ttu-id="926cc-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="926cc-111">-ResourceGroupName</span></span>
<span data-ttu-id="926cc-112">Określa nazwę grupy zasobów kolekcji.</span><span class="sxs-lookup"><span data-stu-id="926cc-112">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="926cc-113">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="926cc-113">-WorkspaceCollectionName</span></span>
<span data-ttu-id="926cc-114">Określa nazwę kolekcji obszaru roboczego usługi Power BI, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="926cc-114">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="926cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="926cc-115">-DefaultProfile</span></span>
<span data-ttu-id="926cc-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="926cc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="926cc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="926cc-117">CommonParameters</span></span>
<span data-ttu-id="926cc-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="926cc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="926cc-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="926cc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="926cc-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="926cc-120">INPUTS</span></span>

## <span data-ttu-id="926cc-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="926cc-121">OUTPUTS</span></span>

### <span data-ttu-id="926cc-122">Microsoft. Azure. Commands. Management. PowerBIEmbedded. models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="926cc-122">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="926cc-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="926cc-123">NOTES</span></span>

## <span data-ttu-id="926cc-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="926cc-124">RELATED LINKS</span></span>

[<span data-ttu-id="926cc-125">Resetowanie — AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="926cc-125">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


