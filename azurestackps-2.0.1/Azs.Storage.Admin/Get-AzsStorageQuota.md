---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054225"
---
# <span data-ttu-id="fc7c7-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="fc7c7-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="fc7c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc7c7-102">SYNOPSIS</span></span>


## <span data-ttu-id="fc7c7-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc7c7-103">SYNTAX</span></span>

### <span data-ttu-id="fc7c7-104">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="fc7c7-104">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc7c7-105">Pobierz</span><span class="sxs-lookup"><span data-stu-id="fc7c7-105">Get</span></span>
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="fc7c7-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="fc7c7-106">GetViaIdentity</span></span>
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="fc7c7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fc7c7-107">DESCRIPTION</span></span>


## <span data-ttu-id="fc7c7-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc7c7-108">EXAMPLES</span></span>

### <span data-ttu-id="fc7c7-109">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="fc7c7-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota
```

<span data-ttu-id="fc7c7-110">Uzyskaj listę przydziałów magazynowania.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-110">Get the list of storage quotas.</span></span>

### <span data-ttu-id="fc7c7-111">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="fc7c7-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

<span data-ttu-id="fc7c7-112">Uzyskaj szczegółowe informacje o określonym przydziale magazynowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-112">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="fc7c7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc7c7-113">PARAMETERS</span></span>

### <span data-ttu-id="fc7c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7c7-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="fc7c7-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fc7c7-115">-InputObject</span></span>
<span data-ttu-id="fc7c7-116">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-116">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="fc7c7-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fc7c7-117">-Location</span></span>


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

### <span data-ttu-id="fc7c7-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc7c7-118">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="fc7c7-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fc7c7-119">-SubscriptionId</span></span>


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

### <span data-ttu-id="fc7c7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7c7-120">CommonParameters</span></span>
<span data-ttu-id="fc7c7-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7c7-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc7c7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7c7-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc7c7-123">INPUTS</span></span>

### <span data-ttu-id="fc7c7-124">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="fc7c7-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="fc7c7-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc7c7-125">OUTPUTS</span></span>

### <span data-ttu-id="fc7c7-126">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="fc7c7-126">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="fc7c7-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc7c7-127">NOTES</span></span>

<span data-ttu-id="fc7c7-128">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fc7c7-129">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="fc7c7-130">INPUTobject <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="fc7c7-130">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="fc7c7-131">`[AccountId <String>]`: Identyfikator konta magazynu wewnętrznego, który nie jest widoczny dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-131">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="fc7c7-132">`[AsyncOperationId <String>]`: Identyfikator operacji asynchronicznej.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-132">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="fc7c7-133">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="fc7c7-133">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fc7c7-134">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-134">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="fc7c7-135">`[QuotaName <String>]`: Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-135">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="fc7c7-136">`[ResourceGroup <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-136">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="fc7c7-137">`[ServiceName <String>]`: Nazwa usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-137">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="fc7c7-138">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fc7c7-138">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="fc7c7-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc7c7-139">RELATED LINKS</span></span>

