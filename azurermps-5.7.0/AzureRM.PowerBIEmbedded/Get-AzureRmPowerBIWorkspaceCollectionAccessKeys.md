---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: 11c1e3c19a6f5767fcfe1120cfa3561a73885f5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527962"
---
# <span data-ttu-id="9e44e-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="9e44e-101">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="9e44e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9e44e-102">SYNOPSIS</span></span>
<span data-ttu-id="9e44e-103">Pobiera bieżące klucze dostępu skojarzone z kolekcją obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="9e44e-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e44e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9e44e-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e44e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9e44e-105">DESCRIPTION</span></span>
<span data-ttu-id="9e44e-106">Polecenie cmdlet **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** pobiera bieżące klucze dostępu skojarzone z kolekcją obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="9e44e-106">The **Get-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="9e44e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9e44e-107">EXAMPLES</span></span>

### <span data-ttu-id="9e44e-108">Przykład 1: uzyskiwanie klawiszy dostępu</span><span class="sxs-lookup"><span data-stu-id="9e44e-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="9e44e-109">To polecenie pobiera klucze programu Access dla kolekcji obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="9e44e-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="9e44e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9e44e-110">PARAMETERS</span></span>

### <span data-ttu-id="9e44e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e44e-111">-DefaultProfile</span></span>
<span data-ttu-id="9e44e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9e44e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e44e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e44e-113">-ResourceGroupName</span></span>
<span data-ttu-id="9e44e-114">Określa nazwę grupy zasobów kolekcji.</span><span class="sxs-lookup"><span data-stu-id="9e44e-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="9e44e-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="9e44e-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="9e44e-116">Określa nazwę kolekcji obszaru roboczego usługi Power BI, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e44e-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="9e44e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e44e-117">CommonParameters</span></span>
<span data-ttu-id="9e44e-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e44e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e44e-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e44e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e44e-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e44e-120">INPUTS</span></span>

### <span data-ttu-id="9e44e-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9e44e-121">None</span></span>
<span data-ttu-id="9e44e-122">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9e44e-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e44e-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9e44e-123">OUTPUTS</span></span>

### <span data-ttu-id="9e44e-124">Microsoft. Azure. Commands. Management. PowerBIEmbedded. models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="9e44e-124">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="9e44e-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9e44e-125">NOTES</span></span>

## <span data-ttu-id="9e44e-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e44e-126">RELATED LINKS</span></span>

[<span data-ttu-id="9e44e-127">Resetowanie — AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="9e44e-127">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


