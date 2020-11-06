---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 230c47e67610cdeea629097f26c73cb2774c5384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548208"
---
# <span data-ttu-id="b7d81-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="b7d81-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="b7d81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7d81-102">SYNOPSIS</span></span>
<span data-ttu-id="b7d81-103">Pobiera klucze interfejsu API dla konta.</span><span class="sxs-lookup"><span data-stu-id="b7d81-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7d81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7d81-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7d81-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b7d81-105">DESCRIPTION</span></span>
<span data-ttu-id="b7d81-106">Polecenie cmdlet **Get-AzureRmCognitiveServicesAccountKey** pobiera klucze interfejsu API dla konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="b7d81-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>

<span data-ttu-id="b7d81-107">Konto usług poznawczych ma dwa klucze API: KEY1 oraz key2.</span><span class="sxs-lookup"><span data-stu-id="b7d81-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="b7d81-108">Klucze umożliwiają interakcję z punktem końcowym konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="b7d81-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>

<span data-ttu-id="b7d81-109">Aby ponownie wygenerować klucz, użyj New-AzureRmCognitiveServicesAccountKey.</span><span class="sxs-lookup"><span data-stu-id="b7d81-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="b7d81-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7d81-110">EXAMPLES</span></span>

## <span data-ttu-id="b7d81-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7d81-111">PARAMETERS</span></span>

### <span data-ttu-id="b7d81-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7d81-112">-DefaultProfile</span></span>
<span data-ttu-id="b7d81-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b7d81-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7d81-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7d81-114">-Name</span></span>
<span data-ttu-id="b7d81-115">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="b7d81-115">Specifies the name of the account.</span></span>
<span data-ttu-id="b7d81-116">To polecenie cmdlet umożliwia pobieranie kluczy dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="b7d81-116">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7d81-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7d81-117">-ResourceGroupName</span></span>
<span data-ttu-id="b7d81-118">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="b7d81-118">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="b7d81-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7d81-119">CommonParameters</span></span>
<span data-ttu-id="b7d81-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7d81-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7d81-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7d81-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7d81-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7d81-122">INPUTS</span></span>

### <span data-ttu-id="b7d81-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b7d81-123">None</span></span>
<span data-ttu-id="b7d81-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b7d81-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7d81-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7d81-125">OUTPUTS</span></span>

### <span data-ttu-id="b7d81-126">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b7d81-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="b7d81-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7d81-127">NOTES</span></span>

## <span data-ttu-id="b7d81-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7d81-128">RELATED LINKS</span></span>

[<span data-ttu-id="b7d81-129">Nowe — AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="b7d81-129">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


