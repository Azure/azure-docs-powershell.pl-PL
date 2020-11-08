---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: efba6588697e34b371622eaa8a5f9a3c349d9ec0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049272"
---
# <span data-ttu-id="ccdf1-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="ccdf1-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="ccdf1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ccdf1-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdf1-103">Generuje ponownie klucz konta.</span><span class="sxs-lookup"><span data-stu-id="ccdf1-103">Regenerates an account key.</span></span>

## <span data-ttu-id="ccdf1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ccdf1-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccdf1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ccdf1-105">DESCRIPTION</span></span>
<span data-ttu-id="ccdf1-106">Polecenie cmdlet **New-AzCognitiveServicesAccountKey** GENERUJE klucz API dla konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="ccdf1-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="ccdf1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ccdf1-107">EXAMPLES</span></span>

### <span data-ttu-id="ccdf1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ccdf1-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="ccdf1-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ccdf1-109">PARAMETERS</span></span>

### <span data-ttu-id="ccdf1-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccdf1-110">-DefaultProfile</span></span>
<span data-ttu-id="ccdf1-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ccdf1-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ccdf1-112">-Force</span><span class="sxs-lookup"><span data-stu-id="ccdf1-112">-Force</span></span>
<span data-ttu-id="ccdf1-113">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ccdf1-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ccdf1-114">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="ccdf1-114">-KeyName</span></span>
<span data-ttu-id="ccdf1-115">Określa nazwę klucza do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="ccdf1-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="ccdf1-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ccdf1-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ccdf1-117">Key1</span><span class="sxs-lookup"><span data-stu-id="ccdf1-117">Key1</span></span>
- <span data-ttu-id="ccdf1-118">Key2</span><span class="sxs-lookup"><span data-stu-id="ccdf1-118">Key2</span></span>

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

### <span data-ttu-id="ccdf1-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ccdf1-119">-Name</span></span>
<span data-ttu-id="ccdf1-120">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="ccdf1-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="ccdf1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccdf1-121">-ResourceGroupName</span></span>
<span data-ttu-id="ccdf1-122">Określa nazwę grupy zasobów, do której przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="ccdf1-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="ccdf1-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ccdf1-123">-Confirm</span></span>
<span data-ttu-id="ccdf1-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccdf1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccdf1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccdf1-125">-WhatIf</span></span>
<span data-ttu-id="ccdf1-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccdf1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccdf1-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ccdf1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccdf1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdf1-128">CommonParameters</span></span>
<span data-ttu-id="ccdf1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccdf1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdf1-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccdf1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdf1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccdf1-131">INPUTS</span></span>

### <span data-ttu-id="ccdf1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ccdf1-132">System.String</span></span>

### <span data-ttu-id="ccdf1-133">Microsoft. Azure. Management. CognitiveServices. models. NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="ccdf1-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="ccdf1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ccdf1-134">OUTPUTS</span></span>

### <span data-ttu-id="ccdf1-135">Microsoft. Azure. Management. CognitiveServices. MODELES. CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ccdf1-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="ccdf1-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ccdf1-136">NOTES</span></span>

## <span data-ttu-id="ccdf1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccdf1-137">RELATED LINKS</span></span>

[<span data-ttu-id="ccdf1-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="ccdf1-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


