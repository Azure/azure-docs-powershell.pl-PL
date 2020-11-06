---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 1c3ebaf3e95c1094b02b73505e471d13015721d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526993"
---
# <span data-ttu-id="e83e3-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e83e3-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="e83e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e83e3-102">SYNOPSIS</span></span>
<span data-ttu-id="e83e3-103">Generuje ponownie klucz konta.</span><span class="sxs-lookup"><span data-stu-id="e83e3-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e83e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e83e3-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e83e3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e83e3-105">DESCRIPTION</span></span>
<span data-ttu-id="e83e3-106">Polecenie cmdlet **New-AzureRmCognitiveServicesAccountKey** GENERUJE klucz API dla konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="e83e3-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="e83e3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e83e3-107">EXAMPLES</span></span>

## <span data-ttu-id="e83e3-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e83e3-108">PARAMETERS</span></span>

### <span data-ttu-id="e83e3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e83e3-109">-DefaultProfile</span></span>
<span data-ttu-id="e83e3-110">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e83e3-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e83e3-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e83e3-111">-Force</span></span>
<span data-ttu-id="e83e3-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e83e3-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e83e3-113">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="e83e3-113">-KeyName</span></span>
<span data-ttu-id="e83e3-114">Określa nazwę klucza do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="e83e3-114">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="e83e3-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e83e3-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e83e3-116">Key1</span><span class="sxs-lookup"><span data-stu-id="e83e3-116">Key1</span></span>
- <span data-ttu-id="e83e3-117">Key2</span><span class="sxs-lookup"><span data-stu-id="e83e3-117">Key2</span></span>

```yaml
Type: KeyName
Parameter Sets: (All)
Aliases: 
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e83e3-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e83e3-118">-Name</span></span>
<span data-ttu-id="e83e3-119">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="e83e3-119">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="e83e3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e83e3-120">-ResourceGroupName</span></span>
<span data-ttu-id="e83e3-121">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="e83e3-121">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="e83e3-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e83e3-122">-Confirm</span></span>
<span data-ttu-id="e83e3-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e83e3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e83e3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e83e3-124">-WhatIf</span></span>
<span data-ttu-id="e83e3-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e83e3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e83e3-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e83e3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e83e3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e83e3-127">CommonParameters</span></span>
<span data-ttu-id="e83e3-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e83e3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e83e3-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e83e3-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e83e3-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e83e3-130">INPUTS</span></span>

### <span data-ttu-id="e83e3-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e83e3-131">None</span></span>
<span data-ttu-id="e83e3-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e83e3-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e83e3-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e83e3-133">OUTPUTS</span></span>

### <span data-ttu-id="e83e3-134">Microsoft. Azure. Management. CognitiveServices. MODELES. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e83e3-134">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="e83e3-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e83e3-135">NOTES</span></span>

## <span data-ttu-id="e83e3-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e83e3-136">RELATED LINKS</span></span>

[<span data-ttu-id="e83e3-137">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="e83e3-137">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


