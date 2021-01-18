---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504223"
---
# <span data-ttu-id="3950a-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="3950a-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="3950a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3950a-102">SYNOPSIS</span></span>
<span data-ttu-id="3950a-103">Zwraca wartość typu BotService określona przez parametry.</span><span class="sxs-lookup"><span data-stu-id="3950a-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="3950a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3950a-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="3950a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3950a-105">DESCRIPTION</span></span>
<span data-ttu-id="3950a-106">Zwraca wartość typu BotService określona przez parametry.</span><span class="sxs-lookup"><span data-stu-id="3950a-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="3950a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3950a-107">EXAMPLES</span></span>

### <span data-ttu-id="3950a-108">Przykład 1. publikowanie BotService na platformie Azure</span><span class="sxs-lookup"><span data-stu-id="3950a-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="3950a-109">Publikowanie BotService na platformie Azure według kodu</span><span class="sxs-lookup"><span data-stu-id="3950a-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="3950a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3950a-110">PARAMETERS</span></span>

### <span data-ttu-id="3950a-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="3950a-111">-CodeDir</span></span>
<span data-ttu-id="3950a-112">Ten parametr definiuje ścieżkę pliku ZIP</span><span class="sxs-lookup"><span data-stu-id="3950a-112">This parameter defines the Path of the ZIP</span></span>

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

### <span data-ttu-id="3950a-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3950a-113">-Name</span></span>
<span data-ttu-id="3950a-114">Ten parametr definiuje nazwę bota.</span><span class="sxs-lookup"><span data-stu-id="3950a-114">This parameter defines the name of the bot.</span></span>

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

### <span data-ttu-id="3950a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3950a-115">-ResourceGroupName</span></span>
<span data-ttu-id="3950a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3950a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3950a-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3950a-117">-Confirm</span></span>
<span data-ttu-id="3950a-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3950a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3950a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3950a-119">-WhatIf</span></span>
<span data-ttu-id="3950a-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3950a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3950a-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3950a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3950a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3950a-122">CommonParameters</span></span>
<span data-ttu-id="3950a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3950a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3950a-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3950a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3950a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3950a-125">INPUTS</span></span>

## <span data-ttu-id="3950a-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3950a-126">OUTPUTS</span></span>

## <span data-ttu-id="3950a-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3950a-127">NOTES</span></span>

<span data-ttu-id="3950a-128">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3950a-128">ALIASES</span></span>

## <span data-ttu-id="3950a-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3950a-129">RELATED LINKS</span></span>

