---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: 22e4f7e115016930e3745e5ce317a3deaa84ad71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981185"
---
# <span data-ttu-id="8b2f8-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="8b2f8-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="8b2f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b2f8-102">SYNOPSIS</span></span>
<span data-ttu-id="8b2f8-103">Ponownie generuje klucz konta.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-103">Regenerates an account key.</span></span>

## <span data-ttu-id="8b2f8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b2f8-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b2f8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b2f8-105">DESCRIPTION</span></span>
<span data-ttu-id="8b2f8-106">Polecenie **cmdlet New-AzCognitiveServicesAccountKey** ponownie generuje klucz interfejsu API dla konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="8b2f8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b2f8-107">EXAMPLES</span></span>

### <span data-ttu-id="8b2f8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b2f8-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="8b2f8-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b2f8-109">PARAMETERS</span></span>

### <span data-ttu-id="8b2f8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b2f8-110">-DefaultProfile</span></span>
<span data-ttu-id="8b2f8-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8b2f8-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b2f8-112">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="8b2f8-112">-Force</span></span>
<span data-ttu-id="8b2f8-113">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b2f8-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8b2f8-114">-KeyName</span></span>
<span data-ttu-id="8b2f8-115">Określa nazwę klucza do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="8b2f8-116">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8b2f8-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8b2f8-117">Klawisz1</span><span class="sxs-lookup"><span data-stu-id="8b2f8-117">Key1</span></span>
- <span data-ttu-id="8b2f8-118">Klawisz 2</span><span class="sxs-lookup"><span data-stu-id="8b2f8-118">Key2</span></span>

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

### <span data-ttu-id="8b2f8-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8b2f8-119">-Name</span></span>
<span data-ttu-id="8b2f8-120">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="8b2f8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b2f8-121">-ResourceGroupName</span></span>
<span data-ttu-id="8b2f8-122">Określa nazwę grupy zasobów, do których przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="8b2f8-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b2f8-123">-Confirm</span></span>
<span data-ttu-id="8b2f8-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b2f8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b2f8-125">-WhatIf</span></span>
<span data-ttu-id="8b2f8-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b2f8-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b2f8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b2f8-128">CommonParameters</span></span>
<span data-ttu-id="8b2f8-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b2f8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b2f8-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b2f8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b2f8-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b2f8-131">INPUTS</span></span>

### <span data-ttu-id="8b2f8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8b2f8-132">System.String</span></span>

### <span data-ttu-id="8b2f8-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span><span class="sxs-lookup"><span data-stu-id="8b2f8-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="8b2f8-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b2f8-134">OUTPUTS</span></span>

### <span data-ttu-id="8b2f8-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8b2f8-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="8b2f8-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b2f8-136">NOTES</span></span>

## <span data-ttu-id="8b2f8-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b2f8-137">RELATED LINKS</span></span>

[<span data-ttu-id="8b2f8-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="8b2f8-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


