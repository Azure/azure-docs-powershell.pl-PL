---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: b0e47d95d8ede448b37ef62e0b9deb7283d293c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526254"
---
# <span data-ttu-id="049f3-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="049f3-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="049f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="049f3-102">SYNOPSIS</span></span>
<span data-ttu-id="049f3-103">Pobiera klucze interfejsu API dla konta.</span><span class="sxs-lookup"><span data-stu-id="049f3-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="049f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="049f3-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="049f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="049f3-105">DESCRIPTION</span></span>
<span data-ttu-id="049f3-106">Polecenie cmdlet **Get-AzureRmCognitiveServicesAccountKey** pobiera klucze interfejsu API dla konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="049f3-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>
<span data-ttu-id="049f3-107">Konto usług poznawczych ma dwa klucze API: KEY1 oraz key2.</span><span class="sxs-lookup"><span data-stu-id="049f3-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="049f3-108">Klucze umożliwiają interakcję z punktem końcowym konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="049f3-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>
<span data-ttu-id="049f3-109">Aby ponownie wygenerować klucz, użyj New-AzureRmCognitiveServicesAccountKey.</span><span class="sxs-lookup"><span data-stu-id="049f3-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="049f3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="049f3-110">EXAMPLES</span></span>

### <span data-ttu-id="049f3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="049f3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="049f3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="049f3-112">PARAMETERS</span></span>

### <span data-ttu-id="049f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="049f3-113">-DefaultProfile</span></span>
<span data-ttu-id="049f3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="049f3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="049f3-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="049f3-115">-Name</span></span>
<span data-ttu-id="049f3-116">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="049f3-116">Specifies the name of the account.</span></span>
<span data-ttu-id="049f3-117">To polecenie cmdlet umożliwia pobieranie kluczy dla tego konta.</span><span class="sxs-lookup"><span data-stu-id="049f3-117">This cmdlet gets the keys for this account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="049f3-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="049f3-118">-ResourceGroupName</span></span>
<span data-ttu-id="049f3-119">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="049f3-119">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="049f3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="049f3-120">CommonParameters</span></span>
<span data-ttu-id="049f3-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="049f3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="049f3-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="049f3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="049f3-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="049f3-123">INPUTS</span></span>

### <span data-ttu-id="049f3-124">System. String</span><span class="sxs-lookup"><span data-stu-id="049f3-124">System.String</span></span>

## <span data-ttu-id="049f3-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="049f3-125">OUTPUTS</span></span>

### <span data-ttu-id="049f3-126">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="049f3-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="049f3-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="049f3-127">NOTES</span></span>

## <span data-ttu-id="049f3-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="049f3-128">RELATED LINKS</span></span>

[<span data-ttu-id="049f3-129">Nowe — AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="049f3-129">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


