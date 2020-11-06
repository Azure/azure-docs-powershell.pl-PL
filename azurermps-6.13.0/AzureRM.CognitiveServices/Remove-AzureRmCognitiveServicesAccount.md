---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/remove-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 2c8496af209cc72ebb6cb9a2ed40ae6033ce7268
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552175"
---
# <span data-ttu-id="10364-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10364-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="10364-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10364-102">SYNOPSIS</span></span>
<span data-ttu-id="10364-103">Usuwa konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="10364-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10364-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10364-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10364-105">Opis</span><span class="sxs-lookup"><span data-stu-id="10364-105">DESCRIPTION</span></span>
<span data-ttu-id="10364-106">Polecenie cmdlet **Remove-AzureRmCognitiveServicesAccount** umożliwia usunięcie określonego konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="10364-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="10364-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10364-107">EXAMPLES</span></span>

### <span data-ttu-id="10364-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10364-108">Example 1</span></span>
<span data-ttu-id="10364-109">To polecenie nie zwraca żadnych zmian.</span><span class="sxs-lookup"><span data-stu-id="10364-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzureRmCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="10364-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10364-110">PARAMETERS</span></span>

### <span data-ttu-id="10364-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10364-111">-DefaultProfile</span></span>
<span data-ttu-id="10364-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="10364-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10364-113">-Force</span><span class="sxs-lookup"><span data-stu-id="10364-113">-Force</span></span>
<span data-ttu-id="10364-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="10364-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="10364-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10364-115">-Name</span></span>
<span data-ttu-id="10364-116">Określa nazwę konta, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="10364-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="10364-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10364-117">-ResourceGroupName</span></span>
<span data-ttu-id="10364-118">Określa nazwę grupy zasobów, do której przypisano konto usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="10364-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="10364-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="10364-119">-Confirm</span></span>
<span data-ttu-id="10364-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10364-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10364-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10364-121">-WhatIf</span></span>
<span data-ttu-id="10364-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10364-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10364-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="10364-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10364-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10364-124">CommonParameters</span></span>
<span data-ttu-id="10364-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10364-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10364-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10364-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10364-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10364-127">INPUTS</span></span>

### <span data-ttu-id="10364-128">System. String</span><span class="sxs-lookup"><span data-stu-id="10364-128">System.String</span></span>

## <span data-ttu-id="10364-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10364-129">OUTPUTS</span></span>

### <span data-ttu-id="10364-130">System. void</span><span class="sxs-lookup"><span data-stu-id="10364-130">System.Void</span></span>

## <span data-ttu-id="10364-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10364-131">NOTES</span></span>

## <span data-ttu-id="10364-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10364-132">RELATED LINKS</span></span>

[<span data-ttu-id="10364-133">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10364-133">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="10364-134">Nowe — AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10364-134">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="10364-135">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10364-135">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


