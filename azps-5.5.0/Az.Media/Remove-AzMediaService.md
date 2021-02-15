---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203625"
---
# <span data-ttu-id="11139-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="11139-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="11139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11139-102">SYNOPSIS</span></span>
<span data-ttu-id="11139-103">Usuwa usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="11139-103">Removes a media service.</span></span>

## <span data-ttu-id="11139-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11139-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11139-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="11139-105">DESCRIPTION</span></span>
<span data-ttu-id="11139-106">Polecenie **cmdlet Remove-AzMediaService** usuwa usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="11139-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="11139-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11139-107">EXAMPLES</span></span>

### <span data-ttu-id="11139-108">Przykład 1. Usuwanie usługi multimediów</span><span class="sxs-lookup"><span data-stu-id="11139-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="11139-109">To polecenie usuwa usługę multimediów o nazwie MediaService0011 z grupy zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="11139-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="11139-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11139-110">PARAMETERS</span></span>

### <span data-ttu-id="11139-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="11139-111">-AccountName</span></span>
<span data-ttu-id="11139-112">Określa nazwę usługi multimediów, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11139-112">Specifies the name of the media service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11139-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11139-113">-DefaultProfile</span></span>
<span data-ttu-id="11139-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="11139-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11139-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="11139-115">-Force</span></span>
<span data-ttu-id="11139-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="11139-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="11139-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11139-117">-ResourceGroupName</span></span>
<span data-ttu-id="11139-118">Określa nazwę grupy zasobów zawierającej usługę multimediów.</span><span class="sxs-lookup"><span data-stu-id="11139-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="11139-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11139-119">-Confirm</span></span>
<span data-ttu-id="11139-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11139-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11139-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11139-121">-WhatIf</span></span>
<span data-ttu-id="11139-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11139-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11139-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11139-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11139-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11139-124">CommonParameters</span></span>
<span data-ttu-id="11139-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11139-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11139-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11139-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11139-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11139-127">INPUTS</span></span>

### <span data-ttu-id="11139-128">System.String</span><span class="sxs-lookup"><span data-stu-id="11139-128">System.String</span></span>

## <span data-ttu-id="11139-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11139-129">OUTPUTS</span></span>

### <span data-ttu-id="11139-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11139-130">System.Boolean</span></span>

## <span data-ttu-id="11139-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11139-131">NOTES</span></span>

## <span data-ttu-id="11139-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11139-132">RELATED LINKS</span></span>

[<span data-ttu-id="11139-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="11139-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="11139-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="11139-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="11139-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="11139-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


