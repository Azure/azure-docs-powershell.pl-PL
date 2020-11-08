---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055974"
---
# <span data-ttu-id="33b35-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="33b35-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="33b35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33b35-102">SYNOPSIS</span></span>


## <span data-ttu-id="33b35-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33b35-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33b35-104">Opis</span><span class="sxs-lookup"><span data-stu-id="33b35-104">DESCRIPTION</span></span>


## <span data-ttu-id="33b35-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33b35-105">EXAMPLES</span></span>

### <span data-ttu-id="33b35-106">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="33b35-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="33b35-107">Zaktualizuj ustawienia przechowywania.</span><span class="sxs-lookup"><span data-stu-id="33b35-107">Update the storage settings.</span></span>

## <span data-ttu-id="33b35-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33b35-108">PARAMETERS</span></span>

### <span data-ttu-id="33b35-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b35-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="33b35-110">-Force</span><span class="sxs-lookup"><span data-stu-id="33b35-110">-Force</span></span>


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

### <span data-ttu-id="33b35-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="33b35-111">-Location</span></span>


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

### <span data-ttu-id="33b35-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="33b35-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="33b35-113">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="33b35-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="33b35-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33b35-114">-Confirm</span></span>
<span data-ttu-id="33b35-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33b35-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33b35-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33b35-116">-WhatIf</span></span>
<span data-ttu-id="33b35-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33b35-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33b35-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="33b35-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33b35-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b35-119">CommonParameters</span></span>
<span data-ttu-id="33b35-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33b35-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b35-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33b35-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b35-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33b35-122">INPUTS</span></span>

## <span data-ttu-id="33b35-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33b35-123">OUTPUTS</span></span>

### <span data-ttu-id="33b35-124">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="33b35-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="33b35-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33b35-125">NOTES</span></span>

## <span data-ttu-id="33b35-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33b35-126">RELATED LINKS</span></span>

