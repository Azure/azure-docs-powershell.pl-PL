---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: E0819A61-157A-4DFD-B492-09C8F1C38E18
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountKey.md
ms.openlocfilehash: efba6588697e34b371622eaa8a5f9a3c349d9ec0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239030"
---
# <span data-ttu-id="76b64-101">New-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="76b64-101">New-AzCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="76b64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76b64-102">SYNOPSIS</span></span>
<span data-ttu-id="76b64-103">Ponownie generuje klucz konta.</span><span class="sxs-lookup"><span data-stu-id="76b64-103">Regenerates an account key.</span></span>

## <span data-ttu-id="76b64-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="76b64-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <KeyName> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76b64-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="76b64-105">DESCRIPTION</span></span>
<span data-ttu-id="76b64-106">Polecenie **cmdlet New-AzCognitiveServicesAccountKey** ponownie generuje klucz interfejsu API dla konta usług Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="76b64-106">The **New-AzCognitiveServicesAccountKey** cmdlet regenerates an API key for a Cognitive Services account.</span></span>

## <span data-ttu-id="76b64-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="76b64-107">EXAMPLES</span></span>

### <span data-ttu-id="76b64-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76b64-108">Example 1</span></span>
```powershell
PS C:\> New-AzCognitiveServicesAccountKey -ResourceGroupName cognitive-services-resource-group -name myluis -keyname Key1

Key1                             Key2
----                             ----
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

## <span data-ttu-id="76b64-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76b64-109">PARAMETERS</span></span>

### <span data-ttu-id="76b64-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76b64-110">-DefaultProfile</span></span>
<span data-ttu-id="76b64-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="76b64-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76b64-112">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="76b64-112">-Force</span></span>
<span data-ttu-id="76b64-113">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="76b64-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="76b64-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="76b64-114">-KeyName</span></span>
<span data-ttu-id="76b64-115">Określa nazwę klucza do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="76b64-115">Specifies the name of the key to regenerate.</span></span>
<span data-ttu-id="76b64-116">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="76b64-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76b64-117">Klawisz1</span><span class="sxs-lookup"><span data-stu-id="76b64-117">Key1</span></span>
- <span data-ttu-id="76b64-118">Klawisz 2</span><span class="sxs-lookup"><span data-stu-id="76b64-118">Key2</span></span>

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

### <span data-ttu-id="76b64-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="76b64-119">-Name</span></span>
<span data-ttu-id="76b64-120">Określa nazwę konta.</span><span class="sxs-lookup"><span data-stu-id="76b64-120">Specifies the name of the account.</span></span>

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

### <span data-ttu-id="76b64-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b64-121">-ResourceGroupName</span></span>
<span data-ttu-id="76b64-122">Określa nazwę grupy zasobów, do których przypisano konto.</span><span class="sxs-lookup"><span data-stu-id="76b64-122">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="76b64-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76b64-123">-Confirm</span></span>
<span data-ttu-id="76b64-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="76b64-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76b64-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76b64-125">-WhatIf</span></span>
<span data-ttu-id="76b64-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76b64-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76b64-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="76b64-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76b64-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b64-128">CommonParameters</span></span>
<span data-ttu-id="76b64-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76b64-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b64-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76b64-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b64-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76b64-131">INPUTS</span></span>

### <span data-ttu-id="76b64-132">System.String</span><span class="sxs-lookup"><span data-stu-id="76b64-132">System.String</span></span>

### <span data-ttu-id="76b64-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span><span class="sxs-lookup"><span data-stu-id="76b64-133">Microsoft.Azure.Management.CognitiveServices.Models.KeyName</span></span>

## <span data-ttu-id="76b64-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76b64-134">OUTPUTS</span></span>

### <span data-ttu-id="76b64-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="76b64-135">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="76b64-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="76b64-136">NOTES</span></span>

## <span data-ttu-id="76b64-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76b64-137">RELATED LINKS</span></span>

[<span data-ttu-id="76b64-138">Get-AzCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="76b64-138">Get-AzCognitiveServicesAccountKey</span></span>](./Get-AzCognitiveServicesAccountKey.md)


