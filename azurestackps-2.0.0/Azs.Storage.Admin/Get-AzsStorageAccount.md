---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 0ddf99277834e69a55b009abcb4b683eebb7a4ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891665"
---
# <span data-ttu-id="2c549-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c549-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="2c549-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c549-102">SYNOPSIS</span></span>
<span data-ttu-id="2c549-103">Zwraca żądane konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="2c549-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="2c549-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c549-104">SYNTAX</span></span>

### <span data-ttu-id="2c549-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2c549-105">List (Default)</span></span>
```
Get-AzsStorageAccount [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Summary]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2c549-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="2c549-106">Get</span></span>
```
Get-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2c549-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2c549-107">GetViaIdentity</span></span>
```
Get-AzsStorageAccount -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2c549-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2c549-108">DESCRIPTION</span></span>
<span data-ttu-id="2c549-109">Zwraca żądane konto magazynu.</span><span class="sxs-lookup"><span data-stu-id="2c549-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="2c549-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c549-110">EXAMPLES</span></span>

### <span data-ttu-id="2c549-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="2c549-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Summary
```

<span data-ttu-id="2c549-112">Uzyskaj listę kont magazynu (podsumowanie).</span><span class="sxs-lookup"><span data-stu-id="2c549-112">Get a list of storage accounts (summary).</span></span>

### <span data-ttu-id="2c549-113">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="2c549-113">Example 2:</span></span>
```powershell
PS C:\> $storageAccount = Get-AzsStorageAccount
PS C:\> $storageAccount | Select Location,Name,AccountStatus,HealthState,Kind | ft
```

<span data-ttu-id="2c549-114">Uzyskaj listę kont magazynu ze szczegółami i wydrukuj stan.</span><span class="sxs-lookup"><span data-stu-id="2c549-114">Get a list of storage account with details and print the status.</span></span>

### <span data-ttu-id="2c549-115">Przykład 3:</span><span class="sxs-lookup"><span data-stu-id="2c549-115">Example 3:</span></span>
```powershell
PS C:\> Get-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 | fl *
```

<span data-ttu-id="2c549-116">Uzyskiwanie szczegółowych informacji dotyczących określonego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2c549-116">Get details of the specified storage account.</span></span>

## <span data-ttu-id="2c549-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c549-117">PARAMETERS</span></span>

### <span data-ttu-id="2c549-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c549-118">-DefaultProfile</span></span>
<span data-ttu-id="2c549-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c549-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c549-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="2c549-120">-Filter</span></span>
<span data-ttu-id="2c549-121">Ciąg filtru</span><span class="sxs-lookup"><span data-stu-id="2c549-121">Filter string</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2c549-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2c549-122">-InputObject</span></span>
<span data-ttu-id="2c549-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="2c549-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2c549-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2c549-124">-Location</span></span>
<span data-ttu-id="2c549-125">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="2c549-125">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2c549-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c549-126">-Name</span></span>
<span data-ttu-id="2c549-127">Identyfikator konta magazynu wewnętrznego, który nie jest widoczny dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="2c549-127">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2c549-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2c549-128">-SubscriptionId</span></span>
<span data-ttu-id="2c549-129">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="2c549-129">Subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2c549-130">— Podsumowanie</span><span class="sxs-lookup"><span data-stu-id="2c549-130">-Summary</span></span>
<span data-ttu-id="2c549-131">Umożliwia określenie, czy są zwracane informacje podsumowujące czy szczegółowe.</span><span class="sxs-lookup"><span data-stu-id="2c549-131">Switch for whether summary or detailed information is returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: $false
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2c549-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c549-132">CommonParameters</span></span>
<span data-ttu-id="2c549-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c549-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c549-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c549-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c549-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c549-135">INPUTS</span></span>

### <span data-ttu-id="2c549-136">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2c549-136">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="2c549-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c549-137">OUTPUTS</span></span>

### <span data-ttu-id="2c549-138">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. Api201908Preview. IStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c549-138">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageAccount</span></span>



## <span data-ttu-id="2c549-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c549-139">NOTES</span></span>

<span data-ttu-id="2c549-140">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="2c549-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2c549-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2c549-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2c549-142">INPUTobject <IStorageAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="2c549-142">INPUTOBJECT <IStorageAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2c549-143">`[AccountId <String>]`: Identyfikator konta magazynu wewnętrznego, który nie jest widoczny dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="2c549-143">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="2c549-144">`[AsyncOperationId <String>]`: Identyfikator operacji asynchronicznej.</span><span class="sxs-lookup"><span data-stu-id="2c549-144">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="2c549-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="2c549-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2c549-146">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="2c549-146">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="2c549-147">`[QuotaName <String>]`: Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="2c549-147">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="2c549-148">`[ResourceGroup <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2c549-148">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="2c549-149">`[ServiceName <String>]`: Nazwa usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="2c549-149">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="2c549-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2c549-150">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="2c549-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c549-151">RELATED LINKS</span></span>

