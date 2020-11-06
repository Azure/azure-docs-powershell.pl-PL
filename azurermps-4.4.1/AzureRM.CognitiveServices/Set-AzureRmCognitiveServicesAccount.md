---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 51338a2cae2aa8bde09ecdea18f0aa74f3727fef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554005"
---
# <span data-ttu-id="1f203-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1f203-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="1f203-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1f203-102">SYNOPSIS</span></span>
<span data-ttu-id="1f203-103">Modyfikuje konto.</span><span class="sxs-lookup"><span data-stu-id="1f203-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f203-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1f203-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f203-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1f203-105">DESCRIPTION</span></span>
<span data-ttu-id="1f203-106">Polecenie cmdlet **Set-AzureRmCognitiveServicesAccount** modyfikuje jednostkę SKU lub Tagi określonego konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="1f203-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="1f203-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1f203-107">EXAMPLES</span></span>

## <span data-ttu-id="1f203-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1f203-108">PARAMETERS</span></span>

### <span data-ttu-id="1f203-109">-Force</span><span class="sxs-lookup"><span data-stu-id="1f203-109">-Force</span></span>
<span data-ttu-id="1f203-110">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1f203-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1f203-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1f203-111">-Name</span></span>
<span data-ttu-id="1f203-112">Określa nazwę konta, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="1f203-112">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="1f203-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f203-113">-ResourceGroupName</span></span>
<span data-ttu-id="1f203-114">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="1f203-114">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="1f203-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="1f203-115">-SkuName</span></span>
<span data-ttu-id="1f203-116">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="1f203-116">Specifies the SKU for the account.</span></span>
<span data-ttu-id="1f203-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1f203-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f203-118">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="1f203-118">F0 (free tier)</span></span>
- <span data-ttu-id="1f203-119">S0</span><span class="sxs-lookup"><span data-stu-id="1f203-119">S0</span></span>
- <span data-ttu-id="1f203-120">S1</span><span class="sxs-lookup"><span data-stu-id="1f203-120">S1</span></span>
- <span data-ttu-id="1f203-121">S2</span><span class="sxs-lookup"><span data-stu-id="1f203-121">S2</span></span>
- <span data-ttu-id="1f203-122">S3</span><span class="sxs-lookup"><span data-stu-id="1f203-122">S3</span></span>
- <span data-ttu-id="1f203-123">Stanu</span><span class="sxs-lookup"><span data-stu-id="1f203-123">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f203-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f203-124">-Tag</span></span>
<span data-ttu-id="1f203-125">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="1f203-125">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f203-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f203-126">-Confirm</span></span>
<span data-ttu-id="1f203-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f203-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f203-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f203-128">-WhatIf</span></span>
<span data-ttu-id="1f203-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f203-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f203-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1f203-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f203-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f203-131">-DefaultProfile</span></span>
<span data-ttu-id="1f203-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f203-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f203-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f203-133">CommonParameters</span></span>
<span data-ttu-id="1f203-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f203-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f203-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f203-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f203-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f203-136">INPUTS</span></span>

## <span data-ttu-id="1f203-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1f203-137">OUTPUTS</span></span>

### <span data-ttu-id="1f203-138">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1f203-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="1f203-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1f203-139">NOTES</span></span>

## <span data-ttu-id="1f203-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f203-140">RELATED LINKS</span></span>

[<span data-ttu-id="1f203-141">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1f203-141">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="1f203-142">Nowe — AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1f203-142">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="1f203-143">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="1f203-143">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
