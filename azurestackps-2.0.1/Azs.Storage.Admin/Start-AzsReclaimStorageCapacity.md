---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054121"
---
# <span data-ttu-id="aa7ec-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="aa7ec-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="aa7ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa7ec-102">SYNOPSIS</span></span>


## <span data-ttu-id="aa7ec-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa7ec-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aa7ec-104">Opis</span><span class="sxs-lookup"><span data-stu-id="aa7ec-104">DESCRIPTION</span></span>


## <span data-ttu-id="aa7ec-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa7ec-105">EXAMPLES</span></span>

### <span data-ttu-id="aa7ec-106">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="aa7ec-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="aa7ec-107">Uruchamianie kolekcji garbage.</span><span class="sxs-lookup"><span data-stu-id="aa7ec-107">Start garbage collection.</span></span>

## <span data-ttu-id="aa7ec-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa7ec-108">PARAMETERS</span></span>

### <span data-ttu-id="aa7ec-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa7ec-109">-AsJob</span></span>


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

### <span data-ttu-id="aa7ec-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa7ec-110">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aa7ec-111">-Force</span><span class="sxs-lookup"><span data-stu-id="aa7ec-111">-Force</span></span>


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

### <span data-ttu-id="aa7ec-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="aa7ec-112">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aa7ec-113">-Nowait</span><span class="sxs-lookup"><span data-stu-id="aa7ec-113">-NoWait</span></span>


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

### <span data-ttu-id="aa7ec-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa7ec-114">-PassThru</span></span>


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

### <span data-ttu-id="aa7ec-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="aa7ec-115">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aa7ec-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa7ec-116">-Confirm</span></span>
<span data-ttu-id="aa7ec-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa7ec-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa7ec-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa7ec-118">-WhatIf</span></span>
<span data-ttu-id="aa7ec-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa7ec-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa7ec-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa7ec-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa7ec-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa7ec-121">CommonParameters</span></span>
<span data-ttu-id="aa7ec-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa7ec-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa7ec-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa7ec-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa7ec-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa7ec-124">INPUTS</span></span>

## <span data-ttu-id="aa7ec-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa7ec-125">OUTPUTS</span></span>

### <span data-ttu-id="aa7ec-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa7ec-126">System.Boolean</span></span>



## <span data-ttu-id="aa7ec-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa7ec-127">NOTES</span></span>

## <span data-ttu-id="aa7ec-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa7ec-128">RELATED LINKS</span></span>

