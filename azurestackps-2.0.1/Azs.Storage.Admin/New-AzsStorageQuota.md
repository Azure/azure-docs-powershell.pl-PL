---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/new-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: bd97eff2a0ed37c309ad0b50927f8231a2da27a6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054131"
---
# <span data-ttu-id="b6166-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b6166-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="b6166-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6166-102">SYNOPSIS</span></span>


## <span data-ttu-id="b6166-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6166-103">SYNTAX</span></span>

### <span data-ttu-id="b6166-104">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b6166-104">CreateExpanded (Default)</span></span>
```
New-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6166-105">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="b6166-105">Create</span></span>
```
New-AzsStorageQuota -Name <String> -QuotaObject <IStorageQuota> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6166-106">Opis</span><span class="sxs-lookup"><span data-stu-id="b6166-106">DESCRIPTION</span></span>


## <span data-ttu-id="b6166-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6166-107">EXAMPLES</span></span>

### <span data-ttu-id="b6166-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="b6166-108">Example 1:</span></span>
```powershell
PS C:\> New-AzsStorageQuota -Name TestQuota -CapacityInGb 123 -NumberOfStorageAccounts 456
```

<span data-ttu-id="b6166-109">Utwórz nowy przydział magazynowania z określonymi wartościami.</span><span class="sxs-lookup"><span data-stu-id="b6166-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="b6166-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6166-110">PARAMETERS</span></span>

### <span data-ttu-id="b6166-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="b6166-111">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b6166-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6166-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="b6166-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b6166-113">-Location</span></span>


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

### <span data-ttu-id="b6166-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6166-114">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b6166-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="b6166-115">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b6166-116">-Przydziałobject</span><span class="sxs-lookup"><span data-stu-id="b6166-116">-QuotaObject</span></span>
<span data-ttu-id="b6166-117">Aby skonstruować, zobacz sekcję notatki dla właściwości przydziałów i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="b6166-117">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b6166-118">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b6166-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="b6166-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6166-119">-Confirm</span></span>
<span data-ttu-id="b6166-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6166-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6166-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6166-121">-WhatIf</span></span>
<span data-ttu-id="b6166-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6166-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6166-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6166-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6166-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6166-124">CommonParameters</span></span>
<span data-ttu-id="b6166-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6166-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6166-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6166-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6166-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6166-127">INPUTS</span></span>

### <span data-ttu-id="b6166-128">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b6166-128">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="b6166-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6166-129">OUTPUTS</span></span>

### <span data-ttu-id="b6166-130">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b6166-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="b6166-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6166-131">NOTES</span></span>

<span data-ttu-id="b6166-132">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b6166-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6166-133">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b6166-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b6166-134">Przydziały <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="b6166-134">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="b6166-135">`[CapacityInGb <Int32?>]`: Maksymalna pojemność (GB).</span><span class="sxs-lookup"><span data-stu-id="b6166-135">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="b6166-136">`[NumberOfStorageAccounts <Int32?>]`: Łączna liczba kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="b6166-136">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="b6166-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6166-137">RELATED LINKS</span></span>

