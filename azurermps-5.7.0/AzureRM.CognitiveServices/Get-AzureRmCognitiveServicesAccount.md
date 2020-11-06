---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41d217579175de3c1de6f36b6850dfd391ca04b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546911"
---
# <span data-ttu-id="2e223-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2e223-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="2e223-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e223-102">SYNOPSIS</span></span>
<span data-ttu-id="2e223-103">Pobiera konto.</span><span class="sxs-lookup"><span data-stu-id="2e223-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e223-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e223-104">SYNTAX</span></span>

### <span data-ttu-id="2e223-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e223-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2e223-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e223-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e223-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2e223-107">DESCRIPTION</span></span>
<span data-ttu-id="2e223-108">Polecenie cmdlet **Get-AzureRmCognitiveServicesAccount** pobiera konta usług poznawczych w grupie zasobów określonym przez parametr *ResoureGroupName* .</span><span class="sxs-lookup"><span data-stu-id="2e223-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="2e223-109">Jeśli nie określisz parametru *ResoureGroupName* , to polecenie cmdlet otrzyma wszystkie konta usług poznawczych dla bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="2e223-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="2e223-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e223-110">EXAMPLES</span></span>

## <span data-ttu-id="2e223-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e223-111">PARAMETERS</span></span>

### <span data-ttu-id="2e223-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e223-112">-DefaultProfile</span></span>
<span data-ttu-id="2e223-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2e223-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e223-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e223-114">-Name</span></span>
<span data-ttu-id="2e223-115">Określa nazwę konta usług poznawczych, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="2e223-115">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e223-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e223-116">-ResourceGroupName</span></span>
<span data-ttu-id="2e223-117">Określa nazwę grupy zasobów, do której przypisano konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="2e223-117">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e223-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e223-118">CommonParameters</span></span>
<span data-ttu-id="2e223-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e223-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e223-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e223-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e223-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e223-121">INPUTS</span></span>

### <span data-ttu-id="2e223-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2e223-122">None</span></span>
<span data-ttu-id="2e223-123">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2e223-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e223-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e223-124">OUTPUTS</span></span>

### <span data-ttu-id="2e223-125">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2e223-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="2e223-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e223-126">NOTES</span></span>

## <span data-ttu-id="2e223-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e223-127">RELATED LINKS</span></span>

[<span data-ttu-id="2e223-128">Nowe — AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2e223-128">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="2e223-129">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2e223-129">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="2e223-130">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2e223-130">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


