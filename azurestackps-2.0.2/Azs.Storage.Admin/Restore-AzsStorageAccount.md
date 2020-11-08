---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055975"
---
# <span data-ttu-id="06424-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="06424-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="06424-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06424-102">SYNOPSIS</span></span>


## <span data-ttu-id="06424-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06424-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="06424-104">Opis</span><span class="sxs-lookup"><span data-stu-id="06424-104">DESCRIPTION</span></span>


## <span data-ttu-id="06424-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06424-105">EXAMPLES</span></span>

### <span data-ttu-id="06424-106">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="06424-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="06424-107">Usuwanie usuniętego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="06424-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="06424-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06424-108">PARAMETERS</span></span>

### <span data-ttu-id="06424-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="06424-109">-AsJob</span></span>


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

### <span data-ttu-id="06424-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06424-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="06424-111">-Force</span><span class="sxs-lookup"><span data-stu-id="06424-111">-Force</span></span>


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

### <span data-ttu-id="06424-112">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="06424-112">-Location</span></span>


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

### <span data-ttu-id="06424-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06424-113">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06424-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="06424-114">-NewAccountName</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="06424-115">-Nowait</span><span class="sxs-lookup"><span data-stu-id="06424-115">-NoWait</span></span>


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

### <span data-ttu-id="06424-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06424-116">-PassThru</span></span>


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

### <span data-ttu-id="06424-117">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="06424-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="06424-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06424-118">-Confirm</span></span>
<span data-ttu-id="06424-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06424-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06424-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06424-120">-WhatIf</span></span>
<span data-ttu-id="06424-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06424-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06424-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="06424-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06424-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06424-123">CommonParameters</span></span>
<span data-ttu-id="06424-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06424-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06424-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06424-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06424-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06424-126">INPUTS</span></span>

## <span data-ttu-id="06424-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06424-127">OUTPUTS</span></span>

### <span data-ttu-id="06424-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="06424-128">System.Boolean</span></span>



## <span data-ttu-id="06424-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06424-129">NOTES</span></span>

## <span data-ttu-id="06424-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06424-130">RELATED LINKS</span></span>

