---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: b89bef906cf54378719c7c6b83dcaff484ced282
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/25/2020
ms.locfileid: "94054359"
---
# <span data-ttu-id="8aaa4-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="8aaa4-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="8aaa4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8aaa4-102">SYNOPSIS</span></span>


## <span data-ttu-id="8aaa4-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8aaa4-103">SYNTAX</span></span>

### <span data-ttu-id="8aaa4-104">Nazwa (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8aaa4-104">Name (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8aaa4-105">Przydziały</span><span class="sxs-lookup"><span data-stu-id="8aaa4-105">QuotaObject</span></span>
```
Set-AzsStorageQuota -QuotaObject <IStorageQuota> [-Location <String>] [-SubscriptionId <String>]
 [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8aaa4-106">Opis</span><span class="sxs-lookup"><span data-stu-id="8aaa4-106">DESCRIPTION</span></span>


## <span data-ttu-id="8aaa4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8aaa4-107">EXAMPLES</span></span>

### <span data-ttu-id="8aaa4-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="8aaa4-108">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -NumberOfStorageAccounts 11 -CapacityInGb 22
```

<span data-ttu-id="8aaa4-109">Zaktualizuj istniejący przydział magazynowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="8aaa4-109">Update an existing storage quota by name.</span></span>

### <span data-ttu-id="8aaa4-110">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="8aaa4-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestUpdateStorageQuota' | Set-AzsStorageQuota -NumberOfStorageAccounts 22 -CapacityInGb 33
```

<span data-ttu-id="8aaa4-111">Zaktualizuj istniejący przydział magazynowania według połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="8aaa4-111">Update an existing storage quota by piping.</span></span>

## <span data-ttu-id="8aaa4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8aaa4-112">PARAMETERS</span></span>

### <span data-ttu-id="8aaa4-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="8aaa4-113">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8aaa4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aaa4-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="8aaa4-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8aaa4-115">-Location</span></span>


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

### <span data-ttu-id="8aaa4-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8aaa4-116">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Name
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8aaa4-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="8aaa4-117">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8aaa4-118">-Przydziałobject</span><span class="sxs-lookup"><span data-stu-id="8aaa4-118">-QuotaObject</span></span>
<span data-ttu-id="8aaa4-119">Aby skonstruować, zobacz sekcję notatki dla właściwości przydziałów i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="8aaa4-119">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: QuotaObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8aaa4-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8aaa4-120">-SubscriptionId</span></span>


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

### <span data-ttu-id="8aaa4-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8aaa4-121">-Confirm</span></span>
<span data-ttu-id="8aaa4-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aaa4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aaa4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aaa4-123">-WhatIf</span></span>
<span data-ttu-id="8aaa4-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8aaa4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aaa4-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8aaa4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aaa4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aaa4-126">CommonParameters</span></span>
<span data-ttu-id="8aaa4-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8aaa4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aaa4-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8aaa4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aaa4-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8aaa4-129">INPUTS</span></span>

### <span data-ttu-id="8aaa4-130">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="8aaa4-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="8aaa4-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8aaa4-131">OUTPUTS</span></span>

### <span data-ttu-id="8aaa4-132">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="8aaa4-132">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="8aaa4-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8aaa4-133">NOTES</span></span>

<span data-ttu-id="8aaa4-134">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8aaa4-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8aaa4-135">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8aaa4-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8aaa4-136">Przydziały <IStorageQuota> :</span><span class="sxs-lookup"><span data-stu-id="8aaa4-136">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="8aaa4-137">`[CapacityInGb <Int32?>]`: Maksymalna pojemność (GB).</span><span class="sxs-lookup"><span data-stu-id="8aaa4-137">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="8aaa4-138">`[NumberOfStorageAccounts <Int32?>]`: Łączna liczba kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="8aaa4-138">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="8aaa4-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8aaa4-139">RELATED LINKS</span></span>

