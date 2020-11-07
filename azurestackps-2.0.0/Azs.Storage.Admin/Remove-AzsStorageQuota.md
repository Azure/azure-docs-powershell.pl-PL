---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/remove-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: 258c7057b8f78ea6de1db506d23c60f679e1ca39
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891657"
---
# <span data-ttu-id="2f40c-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="2f40c-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="2f40c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f40c-102">SYNOPSIS</span></span>


## <span data-ttu-id="2f40c-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f40c-103">SYNTAX</span></span>

### <span data-ttu-id="2f40c-104">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2f40c-104">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2f40c-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2f40c-105">DeleteViaIdentity</span></span>
```
Remove-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2f40c-106">Opis</span><span class="sxs-lookup"><span data-stu-id="2f40c-106">DESCRIPTION</span></span>


## <span data-ttu-id="2f40c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f40c-107">EXAMPLES</span></span>

### <span data-ttu-id="2f40c-108">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="2f40c-108">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsStorageQuota -Name 'TestQuota'
```

<span data-ttu-id="2f40c-109">Usuń przydział magazynowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="2f40c-109">Remove a storage quota by name.</span></span>

### <span data-ttu-id="2f40c-110">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="2f40c-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestQuota' | Remove-AzsStorageQuota
```

<span data-ttu-id="2f40c-111">Usuwanie przydziału miejsca do magazynowania według połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="2f40c-111">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="2f40c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f40c-112">PARAMETERS</span></span>

### <span data-ttu-id="2f40c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f40c-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="2f40c-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2f40c-114">-InputObject</span></span>
<span data-ttu-id="2f40c-115">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="2f40c-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2f40c-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2f40c-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f40c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f40c-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f40c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f40c-118">-PassThru</span></span>


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

### <span data-ttu-id="2f40c-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2f40c-119">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2f40c-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f40c-120">-Confirm</span></span>
<span data-ttu-id="2f40c-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f40c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f40c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f40c-122">-WhatIf</span></span>
<span data-ttu-id="2f40c-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f40c-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f40c-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f40c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f40c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f40c-125">CommonParameters</span></span>
<span data-ttu-id="2f40c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f40c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f40c-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f40c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f40c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f40c-128">INPUTS</span></span>

### <span data-ttu-id="2f40c-129">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2f40c-129">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="2f40c-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f40c-130">OUTPUTS</span></span>

### <span data-ttu-id="2f40c-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f40c-131">System.Boolean</span></span>



## <span data-ttu-id="2f40c-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f40c-132">NOTES</span></span>

<span data-ttu-id="2f40c-133">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2f40c-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2f40c-134">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2f40c-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2f40c-135">INPUTobject <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="2f40c-135">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="2f40c-136">`[AccountId <String>]`: Identyfikator konta magazynu wewnętrznego, który nie jest widoczny dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="2f40c-136">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="2f40c-137">`[AsyncOperationId <String>]`: Identyfikator operacji asynchronicznej.</span><span class="sxs-lookup"><span data-stu-id="2f40c-137">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="2f40c-138">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2f40c-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2f40c-139">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="2f40c-139">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="2f40c-140">`[QuotaName <String>]`: Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="2f40c-140">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="2f40c-141">`[ResourceGroup <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f40c-141">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="2f40c-142">`[ServiceName <String>]`: Nazwa usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="2f40c-142">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="2f40c-143">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2f40c-143">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="2f40c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f40c-144">RELATED LINKS</span></span>

