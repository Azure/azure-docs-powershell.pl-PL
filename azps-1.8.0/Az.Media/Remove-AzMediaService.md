---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: f9d0ee722f828aba251c9776c231338b54c0580c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867408"
---
# <span data-ttu-id="9498b-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9498b-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="9498b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9498b-102">SYNOPSIS</span></span>
<span data-ttu-id="9498b-103">Umożliwia usunięcie usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="9498b-103">Removes a media service.</span></span>

## <span data-ttu-id="9498b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9498b-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9498b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9498b-105">DESCRIPTION</span></span>
<span data-ttu-id="9498b-106">Polecenie cmdlet **Remove-AzMediaService** umożliwia usunięcie usługi multimedialnej.</span><span class="sxs-lookup"><span data-stu-id="9498b-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="9498b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9498b-107">EXAMPLES</span></span>

### <span data-ttu-id="9498b-108">Przykład 1: Usuwanie usługi multimedialnej</span><span class="sxs-lookup"><span data-stu-id="9498b-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="9498b-109">To polecenie powoduje usunięcie usługi multimedialnej o nazwie MediaService0011 w grupie zasobów o nazwie ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="9498b-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="9498b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9498b-110">PARAMETERS</span></span>

### <span data-ttu-id="9498b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9498b-111">-AccountName</span></span>
<span data-ttu-id="9498b-112">Określa nazwę usługi multimedialnej, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9498b-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9498b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9498b-113">-DefaultProfile</span></span>
<span data-ttu-id="9498b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="9498b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9498b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9498b-115">-Force</span></span>
<span data-ttu-id="9498b-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9498b-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9498b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9498b-117">-ResourceGroupName</span></span>
<span data-ttu-id="9498b-118">Określa nazwę grupy zasobów zawierającej usługę Media.</span><span class="sxs-lookup"><span data-stu-id="9498b-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="9498b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9498b-119">-Confirm</span></span>
<span data-ttu-id="9498b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9498b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9498b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9498b-121">-WhatIf</span></span>
<span data-ttu-id="9498b-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9498b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9498b-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9498b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9498b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9498b-124">CommonParameters</span></span>
<span data-ttu-id="9498b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9498b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9498b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9498b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9498b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9498b-127">INPUTS</span></span>

### <span data-ttu-id="9498b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9498b-128">System.String</span></span>

## <span data-ttu-id="9498b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9498b-129">OUTPUTS</span></span>

### <span data-ttu-id="9498b-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9498b-130">System.Boolean</span></span>

## <span data-ttu-id="9498b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9498b-131">NOTES</span></span>

## <span data-ttu-id="9498b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9498b-132">RELATED LINKS</span></span>

[<span data-ttu-id="9498b-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9498b-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="9498b-134">Nowe — AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9498b-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="9498b-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="9498b-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


