---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/new-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/New-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 4701ae347f5a6ea8cd294a0ff75efa51f4d1370d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717640"
---
# <span data-ttu-id="90d52-101">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="90d52-101">New-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="90d52-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90d52-102">SYNOPSIS</span></span>
<span data-ttu-id="90d52-103">Generuje ponownie klucz konta.</span><span class="sxs-lookup"><span data-stu-id="90d52-103">Regenerates an account key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90d52-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90d52-104">SYNTAX</span></span>

```
New-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90d52-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90d52-105">DESCRIPTION</span></span>
<span data-ttu-id="90d52-106">Polecenie cmdlet **New-AzureRmCognitiveServicesAccountKey** GENERUJE klucz API dla konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="90d52-106">The **New-AzureRmCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="90d52-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90d52-107">EXAMPLES</span></span>

### <span data-ttu-id="90d52-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="90d52-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="90d52-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90d52-109">PARAMETERS</span></span>

### <span data-ttu-id="90d52-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d52-110">-DefaultProfile</span></span>
<span data-ttu-id="90d52-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="90d52-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90d52-112">-Force</span><span class="sxs-lookup"><span data-stu-id="90d52-112">-Force</span></span>
<span data-ttu-id="90d52-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="90d52-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="90d52-114">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="90d52-114">-KeyName</span></span>
<span data-ttu-id="90d52-115">Określa nazwę klucza do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="90d52-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="90d52-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="90d52-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90d52-117">Key1</span><span class="sxs-lookup"><span data-stu-id="90d52-117">Key1</span></span>
- <span data-ttu-id="90d52-118">Key2</span><span class="sxs-lookup"><span data-stu-id="90d52-118">Key2</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.KeyName
Parameter Sets: (All)
Aliases:
Accepted values: Key1, Key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90d52-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90d52-119">-Name</span></span>
<span data-ttu-id="90d52-120">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="90d52-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="90d52-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90d52-121">-ResourceGroupName</span></span>
<span data-ttu-id="90d52-122">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="90d52-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="90d52-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90d52-123">-Confirm</span></span>
<span data-ttu-id="90d52-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90d52-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90d52-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90d52-125">-WhatIf</span></span>
<span data-ttu-id="90d52-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90d52-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90d52-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90d52-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90d52-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d52-128">CommonParameters</span></span>
<span data-ttu-id="90d52-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d52-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d52-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d52-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d52-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90d52-131">INPUTS</span></span>

### <span data-ttu-id="90d52-132">System. String</span><span class="sxs-lookup"><span data-stu-id="90d52-132">System.String</span></span>

### <span data-ttu-id="90d52-133">Microsoft. Azure. Management. CognitiveServices. models. NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="90d52-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="90d52-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90d52-134">OUTPUTS</span></span>

### <span data-ttu-id="90d52-135">Microsoft. Azure. Management. CognitiveServices. MODELES. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="90d52-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="90d52-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90d52-136">NOTES</span></span>

## <span data-ttu-id="90d52-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90d52-137">RELATED LINKS</span></span>

[<span data-ttu-id="90d52-138">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="90d52-138">Get-AzureRmCognitiveServicesAccountKey</span></span>](./Get-AzureRmCognitiveServicesAccountKey.md)


