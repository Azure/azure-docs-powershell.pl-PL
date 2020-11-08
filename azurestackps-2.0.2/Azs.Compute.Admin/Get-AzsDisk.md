---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061545"
---
# <span data-ttu-id="3e041-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="3e041-101">Get-AzsDisk</span></span>

## <span data-ttu-id="3e041-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e041-102">SYNOPSIS</span></span>
<span data-ttu-id="3e041-103">Zwraca dysk.</span><span class="sxs-lookup"><span data-stu-id="3e041-103">Returns the disk.</span></span>

## <span data-ttu-id="3e041-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e041-104">SYNTAX</span></span>

### <span data-ttu-id="3e041-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="3e041-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e041-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="3e041-106">Get</span></span>
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e041-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3e041-107">GetViaIdentity</span></span>
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3e041-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3e041-108">DESCRIPTION</span></span>
<span data-ttu-id="3e041-109">Zwraca dysk.</span><span class="sxs-lookup"><span data-stu-id="3e041-109">Returns the disk.</span></span>

## <span data-ttu-id="3e041-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e041-110">EXAMPLES</span></span>

### <span data-ttu-id="3e041-111">Przykład 1: pobieranie wszystkich dysków</span><span class="sxs-lookup"><span data-stu-id="3e041-111">Example 1: Get All Disks</span></span> 
```powershell
PS C:\> Get-AzsDisk
```

<span data-ttu-id="3e041-112">Bez żadnych parametrów `Get-AzsDisk` zostanie wystawiona lista wszystkich dysków.</span><span class="sxs-lookup"><span data-stu-id="3e041-112">Without any parameters, `Get-AzsDisk` will list all Disks.</span></span>

### <span data-ttu-id="3e041-113">Przykład 2: uzyskiwanie dysku według nazwy</span><span class="sxs-lookup"><span data-stu-id="3e041-113">Example 2: Get a Disk by Name</span></span>
```powershell
PS C:\> Get-AzsDisk -Name "426b8945-8a24-42ad-acdc-c26f16202489"

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="3e041-114">Określ dysk, `Name` Aby go pobrać.</span><span class="sxs-lookup"><span data-stu-id="3e041-114">Specify a disk by its `Name` to retrieve it.</span></span>

### <span data-ttu-id="3e041-115">Przykład 3: Uzyskaj określoną liczbę dysków</span><span class="sxs-lookup"><span data-stu-id="3e041-115">Example 3: Get a Specified number of Disks</span></span>
```powershell
PS C:\>  Get-AzsDisk -Count 3

ActualSizeGb    : 24
DiskId          : 20f1619e-4210-47f6-81e6-b89e3028df06
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/20f1619e-4210-47f6-81e6-b89e3028df06
Location        : northwest
ManagedBy       :
Name            : northwest/20f1619e-4210-47f6-81e6-b89e3028df06
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/RG1/providers/Microsoft.Compute/Di
                  sks/TEST_OsDisk_1_20f1619e421047f681e6b89e3028df06

ActualSizeGb    : 24
DiskId          : 38a767e4-4ceb-49fb-a53c-48de9b08aaae
DiskSku         : Standard_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/38a767e4-4ceb-49fb-a53c-48de9b08aaae
Location        : northwest
ManagedBy       :
Name            : northwest/38a767e4-4ceb-49fb-a53c-48de9b08aaae
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/SCTE/providers/Microsoft.Compute/D
                  isks/SCTETest_OsDisk_1_38a767e44ceb49fba53c48de9b08aaae

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="3e041-116">Użyj `Count` parametru, aby pobrać określoną liczbę dysków.</span><span class="sxs-lookup"><span data-stu-id="3e041-116">Use the `Count` parameter to retrieve a specific number of disks.</span></span>

### <span data-ttu-id="3e041-117">Przykład 4: pobieranie wszystkich dysków w określonej lokalizacji</span><span class="sxs-lookup"><span data-stu-id="3e041-117">Example 4: Get all disks in specific location</span></span>
```powershell
PS C:\> Get-AzsDisk -Status All -ScaleUnit s-cluster -VolumeLabel Objstore_4

ActualSizeGb    : 2
DiskId          : e4732f76-0753-40ec-80f5-8effdd0b437d
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/e4732f76-0753-40ec-80f5-8effdd0b437d
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/e4732f76-0753-40ec-80f5-8effdd0b437d
ProvisionSizeGb : 30
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/test1_OsDisk_1_e4732f76075340ec80f58effdd0b437d

ActualSizeGb    : 1
DiskId          : 0485cbc9-1efa-43bd-86c2-0e201d79c528
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/0485cbc9-1efa-43bd-86c2-0e201d79c528
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/0485cbc9-1efa-43bd-86c2-0e201d79c528
ProvisionSizeGb : 64
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/TESTRG1/providers/Microsoft.Compute/Disks/gpsdisk

ActualSizeGb    : 1
DiskId          : 137893db-e7ce-4907-a488-b35c5e928614
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/137893db-e7ce-4907-a488-b35c5e928614
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/137893db-e7ce-4907-a488-b35c5e928614
ProvisionSizeGb : 55
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/testdd
```

<span data-ttu-id="3e041-118">`ScaleUnit` `VolumeLabel` Aby wyświetlić wszystkie dyski w określonej lokalizacji, użyj parametru lub.</span><span class="sxs-lookup"><span data-stu-id="3e041-118">Use the `ScaleUnit` or `VolumeLabel` parameter to list all disks in specific location</span></span>

## <span data-ttu-id="3e041-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e041-119">PARAMETERS</span></span>

### <span data-ttu-id="3e041-120">-Count</span><span class="sxs-lookup"><span data-stu-id="3e041-120">-Count</span></span>
<span data-ttu-id="3e041-121">Maksymalna liczba dysków, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="3e041-121">The maximum number of disks to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e041-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e041-122">-DefaultProfile</span></span>
<span data-ttu-id="3e041-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e041-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e041-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3e041-124">-InputObject</span></span>
<span data-ttu-id="3e041-125">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3e041-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3e041-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3e041-126">-Location</span></span>
<span data-ttu-id="3e041-127">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="3e041-127">Location of the resource.</span></span>

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

### <span data-ttu-id="3e041-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e041-128">-Name</span></span>
<span data-ttu-id="3e041-129">Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="3e041-129">The disk guid as identity.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e041-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="3e041-130">-ScaleUnit</span></span>
<span data-ttu-id="3e041-131">Jednostka skali, do której należy zasób.</span><span class="sxs-lookup"><span data-stu-id="3e041-131">The scale unit which the resource belongs to.</span></span>

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

### <span data-ttu-id="3e041-132">-SharePath</span><span class="sxs-lookup"><span data-stu-id="3e041-132">-SharePath</span></span>
<span data-ttu-id="3e041-133">Udział, do którego należy zasób.</span><span class="sxs-lookup"><span data-stu-id="3e041-133">The share which the resource belongs to.</span></span>

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

### <span data-ttu-id="3e041-134">-Start</span><span class="sxs-lookup"><span data-stu-id="3e041-134">-Start</span></span>
<span data-ttu-id="3e041-135">Indeks początkowy dysków w zapytaniu.</span><span class="sxs-lookup"><span data-stu-id="3e041-135">The start index of disks in query.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3e041-136">-Status</span><span class="sxs-lookup"><span data-stu-id="3e041-136">-Status</span></span>
<span data-ttu-id="3e041-137">Parametry stanu dysku.</span><span class="sxs-lookup"><span data-stu-id="3e041-137">The parameters of disk state.</span></span>

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

### <span data-ttu-id="3e041-138">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3e041-138">-SubscriptionId</span></span>
<span data-ttu-id="3e041-139">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e041-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e041-140">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3e041-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3e041-141">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e041-141">-UserSubscriptionId</span></span>
<span data-ttu-id="3e041-142">Identyfikator subskrypcji użytkownika, do którego należy zasób.</span><span class="sxs-lookup"><span data-stu-id="3e041-142">User Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="3e041-143">-VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="3e041-143">-VolumeLabel</span></span>
<span data-ttu-id="3e041-144">Etykieta woluminu, do którego należy zasób.</span><span class="sxs-lookup"><span data-stu-id="3e041-144">The volume label of the volume which the resource belongs to.</span></span>

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

### <span data-ttu-id="3e041-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e041-145">CommonParameters</span></span>
<span data-ttu-id="3e041-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e041-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e041-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e041-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e041-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e041-148">INPUTS</span></span>

### <span data-ttu-id="3e041-149">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3e041-149">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="3e041-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e041-150">OUTPUTS</span></span>

### <span data-ttu-id="3e041-151">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20180730Preview. IDisk</span><span class="sxs-lookup"><span data-stu-id="3e041-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk</span></span>



## <span data-ttu-id="3e041-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e041-152">NOTES</span></span>

<span data-ttu-id="3e041-153">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3e041-153">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e041-154">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3e041-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3e041-155">INPUTobject <IComputeAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="3e041-155">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3e041-156">`[DiskId <String>]`: Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="3e041-156">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="3e041-157">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3e041-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e041-158">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="3e041-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="3e041-159">`[MigrationId <String>]`: Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="3e041-159">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="3e041-160">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="3e041-160">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="3e041-161">`[Publisher <String>]`: Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="3e041-161">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="3e041-162">`[QuotaName <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="3e041-162">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="3e041-163">`[Sku <String>]`: Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="3e041-163">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="3e041-164">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3e041-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3e041-165">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3e041-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3e041-166">`[Type <String>]`: Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="3e041-166">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="3e041-167">`[Version <String>]`: Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="3e041-167">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="3e041-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e041-168">RELATED LINKS</span></span>

