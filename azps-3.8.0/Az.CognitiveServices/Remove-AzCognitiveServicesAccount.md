---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049267"
---
# <span data-ttu-id="58305-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="58305-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="58305-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58305-102">SYNOPSIS</span></span>
<span data-ttu-id="58305-103">Usuwa konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="58305-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="58305-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58305-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58305-105">Opis</span><span class="sxs-lookup"><span data-stu-id="58305-105">DESCRIPTION</span></span>
<span data-ttu-id="58305-106">Polecenie cmdlet **Remove-AzCognitiveServicesAccount** umożliwia usunięcie określonego konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="58305-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="58305-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58305-107">EXAMPLES</span></span>

### <span data-ttu-id="58305-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="58305-108">Example 1</span></span>
<span data-ttu-id="58305-109">To polecenie nie zwraca żadnych zmian.</span><span class="sxs-lookup"><span data-stu-id="58305-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="58305-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58305-110">PARAMETERS</span></span>

### <span data-ttu-id="58305-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58305-111">-DefaultProfile</span></span>
<span data-ttu-id="58305-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="58305-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58305-113">-Force</span><span class="sxs-lookup"><span data-stu-id="58305-113">-Force</span></span>
<span data-ttu-id="58305-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="58305-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58305-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="58305-115">-Name</span></span>
<span data-ttu-id="58305-116">Określa nazwę konta, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="58305-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="58305-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58305-117">-ResourceGroupName</span></span>
<span data-ttu-id="58305-118">Określa nazwę grupy zasobów, do której przypisano konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="58305-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="58305-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="58305-119">-Confirm</span></span>
<span data-ttu-id="58305-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58305-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58305-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58305-121">-WhatIf</span></span>
<span data-ttu-id="58305-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58305-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58305-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="58305-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58305-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58305-124">CommonParameters</span></span>
<span data-ttu-id="58305-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58305-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58305-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58305-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58305-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58305-127">INPUTS</span></span>

### <span data-ttu-id="58305-128">System. String</span><span class="sxs-lookup"><span data-stu-id="58305-128">System.String</span></span>

## <span data-ttu-id="58305-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58305-129">OUTPUTS</span></span>

### <span data-ttu-id="58305-130">System. void</span><span class="sxs-lookup"><span data-stu-id="58305-130">System.Void</span></span>

## <span data-ttu-id="58305-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58305-131">NOTES</span></span>

## <span data-ttu-id="58305-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58305-132">RELATED LINKS</span></span>

[<span data-ttu-id="58305-133">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="58305-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="58305-134">Nowe — AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="58305-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="58305-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="58305-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


