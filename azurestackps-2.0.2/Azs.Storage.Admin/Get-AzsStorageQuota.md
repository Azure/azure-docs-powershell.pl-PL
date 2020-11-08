---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055578"
---
# <span data-ttu-id="b7251-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b7251-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="b7251-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7251-102">SYNOPSIS</span></span>


## <span data-ttu-id="b7251-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7251-103">SYNTAX</span></span>

### <span data-ttu-id="b7251-104">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b7251-104">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7251-105">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b7251-105">Get</span></span>
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b7251-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b7251-106">GetViaIdentity</span></span>
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b7251-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b7251-107">DESCRIPTION</span></span>


## <span data-ttu-id="b7251-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7251-108">EXAMPLES</span></span>

### <span data-ttu-id="b7251-109">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="b7251-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota
```

<span data-ttu-id="b7251-110">Uzyskaj listę przydziałów magazynowania.</span><span class="sxs-lookup"><span data-stu-id="b7251-110">Get the list of storage quotas.</span></span>

### <span data-ttu-id="b7251-111">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="b7251-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

<span data-ttu-id="b7251-112">Uzyskaj szczegółowe informacje o określonym przydziale magazynowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b7251-112">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="b7251-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7251-113">PARAMETERS</span></span>

### <span data-ttu-id="b7251-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7251-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="b7251-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b7251-115">-InputObject</span></span>
<span data-ttu-id="b7251-116">Aby skonstruować, zobacz sekcję notatki dla właściwości INPUTobject i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="b7251-116">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7251-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b7251-117">-Location</span></span>


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

### <span data-ttu-id="b7251-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b7251-118">-Name</span></span>


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

### <span data-ttu-id="b7251-119">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b7251-119">-SubscriptionId</span></span>


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

### <span data-ttu-id="b7251-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7251-120">CommonParameters</span></span>
<span data-ttu-id="b7251-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7251-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7251-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7251-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7251-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7251-123">INPUTS</span></span>

### <span data-ttu-id="b7251-124">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. IStorageAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b7251-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="b7251-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7251-125">OUTPUTS</span></span>

### <span data-ttu-id="b7251-126">Microsoft. Azure. PowerShell. polecenia. StorageAdmin. models. Api201908Preview. IStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b7251-126">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="b7251-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7251-127">NOTES</span></span>

<span data-ttu-id="b7251-128">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b7251-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7251-129">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7251-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b7251-130">INPUTobject <IStorageAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="b7251-130">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="b7251-131">`[AccountId <String>]`: Identyfikator konta magazynu wewnętrznego, który nie jest widoczny dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="b7251-131">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="b7251-132">`[AsyncOperationId <String>]`: Identyfikator operacji asynchronicznej.</span><span class="sxs-lookup"><span data-stu-id="b7251-132">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="b7251-133">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b7251-133">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7251-134">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="b7251-134">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="b7251-135">`[QuotaName <String>]`: Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="b7251-135">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="b7251-136">`[ResourceGroup <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7251-136">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="b7251-137">`[ServiceName <String>]`: Nazwa usługi magazynu.</span><span class="sxs-lookup"><span data-stu-id="b7251-137">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="b7251-138">`[SubscriptionId <String>]`: Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b7251-138">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="b7251-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7251-139">RELATED LINKS</span></span>

