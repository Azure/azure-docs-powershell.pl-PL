---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893973"
---
# <span data-ttu-id="560bb-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="560bb-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="560bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="560bb-102">SYNOPSIS</span></span>


## <span data-ttu-id="560bb-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="560bb-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="560bb-104">Opis</span><span class="sxs-lookup"><span data-stu-id="560bb-104">DESCRIPTION</span></span>


## <span data-ttu-id="560bb-105">Przykłady</span><span class="sxs-lookup"><span data-stu-id="560bb-105">EXAMPLES</span></span>

### <span data-ttu-id="560bb-106">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="560bb-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="560bb-107">Zaktualizuj ustawienia przechowywania.</span><span class="sxs-lookup"><span data-stu-id="560bb-107">Update the storage settings.</span></span>

## <span data-ttu-id="560bb-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="560bb-108">PARAMETERS</span></span>

### <span data-ttu-id="560bb-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="560bb-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="560bb-110">-Force</span><span class="sxs-lookup"><span data-stu-id="560bb-110">-Force</span></span>


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

### <span data-ttu-id="560bb-111">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="560bb-111">-Location</span></span>


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

### <span data-ttu-id="560bb-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="560bb-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


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

### <span data-ttu-id="560bb-113">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="560bb-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="560bb-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="560bb-114">-Confirm</span></span>
<span data-ttu-id="560bb-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="560bb-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="560bb-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="560bb-116">-WhatIf</span></span>
<span data-ttu-id="560bb-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="560bb-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="560bb-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="560bb-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="560bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="560bb-119">CommonParameters</span></span>
<span data-ttu-id="560bb-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="560bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="560bb-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="560bb-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="560bb-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="560bb-122">INPUTS</span></span>

## <span data-ttu-id="560bb-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="560bb-123">OUTPUTS</span></span>

### <span data-ttu-id="560bb-124">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="560bb-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="560bb-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="560bb-125">NOTES</span></span>

## <span data-ttu-id="560bb-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="560bb-126">RELATED LINKS</span></span>

