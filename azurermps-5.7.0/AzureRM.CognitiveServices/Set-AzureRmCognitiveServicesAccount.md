---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a31ee6979a73e4637e683a5b388f4265bf53d2a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553019"
---
# <span data-ttu-id="a4b67-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4b67-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="a4b67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4b67-102">SYNOPSIS</span></span>
<span data-ttu-id="a4b67-103">Modyfikuje konto.</span><span class="sxs-lookup"><span data-stu-id="a4b67-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4b67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4b67-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4b67-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4b67-105">DESCRIPTION</span></span>
<span data-ttu-id="a4b67-106">Polecenie cmdlet **Set-AzureRmCognitiveServicesAccount** modyfikuje jednostkę SKU lub Tagi określonego konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="a4b67-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="a4b67-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4b67-107">EXAMPLES</span></span>

## <span data-ttu-id="a4b67-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4b67-108">PARAMETERS</span></span>

### <span data-ttu-id="a4b67-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4b67-109">-DefaultProfile</span></span>
<span data-ttu-id="a4b67-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a4b67-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4b67-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a4b67-111">-Force</span></span>
<span data-ttu-id="a4b67-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a4b67-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b67-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4b67-113">-Name</span></span>
<span data-ttu-id="a4b67-114">Określa nazwę konta, które ma zostać zmodyfikowane.</span><span class="sxs-lookup"><span data-stu-id="a4b67-114">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="a4b67-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4b67-115">-ResourceGroupName</span></span>
<span data-ttu-id="a4b67-116">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="a4b67-116">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="a4b67-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a4b67-117">-SkuName</span></span>
<span data-ttu-id="a4b67-118">Określa jednostkę SKU konta.</span><span class="sxs-lookup"><span data-stu-id="a4b67-118">Specifies the SKU for the account.</span></span>
<span data-ttu-id="a4b67-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a4b67-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a4b67-120">F0 (warstwa wolna)</span><span class="sxs-lookup"><span data-stu-id="a4b67-120">F0 (free tier)</span></span>
- <span data-ttu-id="a4b67-121">S0</span><span class="sxs-lookup"><span data-stu-id="a4b67-121">S0</span></span>
- <span data-ttu-id="a4b67-122">S1</span><span class="sxs-lookup"><span data-stu-id="a4b67-122">S1</span></span>
- <span data-ttu-id="a4b67-123">S2</span><span class="sxs-lookup"><span data-stu-id="a4b67-123">S2</span></span>
- <span data-ttu-id="a4b67-124">S3</span><span class="sxs-lookup"><span data-stu-id="a4b67-124">S3</span></span>
- <span data-ttu-id="a4b67-125">Stanu</span><span class="sxs-lookup"><span data-stu-id="a4b67-125">S4</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b67-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="a4b67-126">-Tag</span></span>
<span data-ttu-id="a4b67-127">Określa tag jako parę nazwa/wartość.</span><span class="sxs-lookup"><span data-stu-id="a4b67-127">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4b67-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4b67-128">-Confirm</span></span>
<span data-ttu-id="a4b67-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4b67-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b67-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4b67-130">-WhatIf</span></span>
<span data-ttu-id="a4b67-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4b67-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4b67-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4b67-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4b67-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4b67-133">CommonParameters</span></span>
<span data-ttu-id="a4b67-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4b67-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4b67-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4b67-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4b67-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4b67-136">INPUTS</span></span>

### <span data-ttu-id="a4b67-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a4b67-137">None</span></span>
<span data-ttu-id="a4b67-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a4b67-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4b67-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4b67-139">OUTPUTS</span></span>

### <span data-ttu-id="a4b67-140">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4b67-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="a4b67-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4b67-141">NOTES</span></span>

## <span data-ttu-id="a4b67-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4b67-142">RELATED LINKS</span></span>

[<span data-ttu-id="a4b67-143">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4b67-143">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a4b67-144">Nowe — AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4b67-144">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="a4b67-145">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a4b67-145">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
