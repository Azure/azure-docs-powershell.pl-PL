---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 3FED0088-47DA-4565-B9F0-DACF9B2DC0C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/get-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Get-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: b9b6092035d97aed8f70137c4157bfb80bf3f62a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708777"
---
# <span data-ttu-id="b34bd-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b34bd-101">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="b34bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b34bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b34bd-103">Pobiera bieżące klucze dostępu skojarzone z kolekcją obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="b34bd-103">Gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="b34bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b34bd-104">SYNTAX</span></span>

```
Get-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b34bd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b34bd-105">DESCRIPTION</span></span>
<span data-ttu-id="b34bd-106">Polecenie cmdlet **Get-AzPowerBIWorkspaceCollectionAccessKey** pobiera bieżące klucze dostępu skojarzone z kolekcją obszarów roboczych usługi Power BI.</span><span class="sxs-lookup"><span data-stu-id="b34bd-106">The **Get-AzPowerBIWorkspaceCollectionAccessKey** cmdlet gets the current access keys associated with a Power BI workspace collection.</span></span>

## <span data-ttu-id="b34bd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b34bd-107">EXAMPLES</span></span>

### <span data-ttu-id="b34bd-108">Przykład 1: uzyskiwanie klawiszy dostępu</span><span class="sxs-lookup"><span data-stu-id="b34bd-108">Example 1: Get access keys</span></span>
```
PS C:\>Get-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="b34bd-109">To polecenie pobiera klucze programu Access dla kolekcji obszarów roboczych o nazwie WCN11 w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b34bd-109">This command gets access keys for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="b34bd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b34bd-110">PARAMETERS</span></span>

### <span data-ttu-id="b34bd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34bd-111">-DefaultProfile</span></span>
<span data-ttu-id="b34bd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b34bd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b34bd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b34bd-113">-ResourceGroupName</span></span>
<span data-ttu-id="b34bd-114">Określa nazwę grupy zasobów kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b34bd-114">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="b34bd-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="b34bd-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="b34bd-116">Określa nazwę kolekcji obszaru roboczego usługi Power BI, na której działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b34bd-116">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="b34bd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34bd-117">CommonParameters</span></span>
<span data-ttu-id="b34bd-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b34bd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34bd-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b34bd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34bd-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b34bd-120">INPUTS</span></span>

### <span data-ttu-id="b34bd-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b34bd-121">System.String</span></span>

## <span data-ttu-id="b34bd-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b34bd-122">OUTPUTS</span></span>

### <span data-ttu-id="b34bd-123">Microsoft. Azure. Commands. Management. PowerBIEmbedded. models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b34bd-123">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="b34bd-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b34bd-124">NOTES</span></span>

## <span data-ttu-id="b34bd-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b34bd-125">RELATED LINKS</span></span>

[<span data-ttu-id="b34bd-126">Resetowanie — AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="b34bd-126">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Reset-AzPowerBIWorkspaceCollectionAccessKey.md)


