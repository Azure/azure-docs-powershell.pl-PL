---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: c4419707c9c536a21e5fdc8aa39326b02e21937c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546988"
---
# <span data-ttu-id="10f7f-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10f7f-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="10f7f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="10f7f-103">Pobiera konto.</span><span class="sxs-lookup"><span data-stu-id="10f7f-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10f7f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10f7f-104">SYNTAX</span></span>

### <span data-ttu-id="10f7f-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="10f7f-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10f7f-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="10f7f-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10f7f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="10f7f-107">DESCRIPTION</span></span>
<span data-ttu-id="10f7f-108">Polecenie cmdlet **Get-AzureRmCognitiveServicesAccount** pobiera konta usług poznawczych w grupie zasobów określonym przez parametr *ResoureGroupName* .</span><span class="sxs-lookup"><span data-stu-id="10f7f-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="10f7f-109">Jeśli nie określisz parametru *ResoureGroupName* , to polecenie cmdlet otrzyma wszystkie konta usług poznawczych dla bieżącego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="10f7f-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="10f7f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10f7f-110">EXAMPLES</span></span>

## <span data-ttu-id="10f7f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10f7f-111">PARAMETERS</span></span>

### <span data-ttu-id="10f7f-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10f7f-112">-Name</span></span>
<span data-ttu-id="10f7f-113">Określa nazwę konta usług poznawczych, które ma zostać pozyskane.</span><span class="sxs-lookup"><span data-stu-id="10f7f-113">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f7f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10f7f-114">-ResourceGroupName</span></span>
<span data-ttu-id="10f7f-115">Określa nazwę grupy zasobów, do której przypisano konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="10f7f-115">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10f7f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10f7f-116">-DefaultProfile</span></span>
<span data-ttu-id="10f7f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10f7f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10f7f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10f7f-118">CommonParameters</span></span>
<span data-ttu-id="10f7f-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10f7f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10f7f-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10f7f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10f7f-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10f7f-121">INPUTS</span></span>

## <span data-ttu-id="10f7f-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10f7f-122">OUTPUTS</span></span>

### <span data-ttu-id="10f7f-123">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10f7f-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="10f7f-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10f7f-124">NOTES</span></span>

## <span data-ttu-id="10f7f-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10f7f-125">RELATED LINKS</span></span>

[<span data-ttu-id="10f7f-126">Nowe — AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10f7f-126">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="10f7f-127">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10f7f-127">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="10f7f-128">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10f7f-128">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


