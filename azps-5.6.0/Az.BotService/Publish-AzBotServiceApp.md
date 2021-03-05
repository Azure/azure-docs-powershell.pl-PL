---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 551428a1c5d1737d32aeddf2dd5653586d1dbfbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965082"
---
# <span data-ttu-id="c9b6f-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="c9b6f-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="c9b6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9b6f-103">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="c9b6f-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="c9b6f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c9b6f-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c9b6f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c9b6f-105">DESCRIPTION</span></span>
<span data-ttu-id="c9b6f-106">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="c9b6f-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="c9b6f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c9b6f-107">EXAMPLES</span></span>

### <span data-ttu-id="c9b6f-108">Przykład 1. Publikowanie usługi BotService na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="c9b6f-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="c9b6f-109">Publikowanie usługi BotService na platformie Azure według kodu</span><span class="sxs-lookup"><span data-stu-id="c9b6f-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="c9b6f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9b6f-110">PARAMETERS</span></span>

### <span data-ttu-id="c9b6f-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="c9b6f-111">-CodeDir</span></span>
<span data-ttu-id="c9b6f-112">Ten parametr definiuje ścieżkę pliku ZIP</span><span class="sxs-lookup"><span data-stu-id="c9b6f-112">This parameter defines the Path of the ZIP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b6f-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c9b6f-113">-Name</span></span>
<span data-ttu-id="c9b6f-114">Ten parametr definiuje nazwę bota.</span><span class="sxs-lookup"><span data-stu-id="c9b6f-114">This parameter defines the name of the bot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b6f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9b6f-115">-ResourceGroupName</span></span>
<span data-ttu-id="c9b6f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c9b6f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b6f-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9b6f-117">-Confirm</span></span>
<span data-ttu-id="c9b6f-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c9b6f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b6f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9b6f-119">-WhatIf</span></span>
<span data-ttu-id="c9b6f-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9b6f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9b6f-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c9b6f-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9b6f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9b6f-122">CommonParameters</span></span>
<span data-ttu-id="c9b6f-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9b6f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9b6f-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9b6f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9b6f-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9b6f-125">INPUTS</span></span>

## <span data-ttu-id="c9b6f-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9b6f-126">OUTPUTS</span></span>

## <span data-ttu-id="c9b6f-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c9b6f-127">NOTES</span></span>

<span data-ttu-id="c9b6f-128">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c9b6f-128">ALIASES</span></span>

## <span data-ttu-id="c9b6f-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9b6f-129">RELATED LINKS</span></span>

