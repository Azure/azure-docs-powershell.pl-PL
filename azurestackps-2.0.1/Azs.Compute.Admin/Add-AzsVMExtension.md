---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsvmextension
schema: 2.0.0
ms.openlocfilehash: a9c5a207d478fe40181150206990cb47ad4e45d5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054307"
---
# <span data-ttu-id="75e12-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="75e12-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="75e12-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="75e12-102">SYNOPSIS</span></span>
<span data-ttu-id="75e12-103">Utwórz obraz rozszerzenia maszyny wirtualnej w programie Publisher i w wersji.</span><span class="sxs-lookup"><span data-stu-id="75e12-103">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="75e12-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="75e12-104">SYNTAX</span></span>

### <span data-ttu-id="75e12-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="75e12-105">CreateExpanded (Default)</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-ComputeRole <String>] [-IsSystemExtension] [-PropertiesPublisher <String>]
 [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>] [-SupportMultipleExtensions]
 [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="75e12-106">Tworzonych</span><span class="sxs-lookup"><span data-stu-id="75e12-106">Create</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> -Extension <IVMExtensionParameters>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="75e12-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="75e12-107">CreateViaIdentity</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> -Extension <IVMExtensionParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75e12-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="75e12-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> [-Publisher <String>] [-ComputeRole <String>]
 [-IsSystemExtension] [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>]
 [-SupportMultipleExtensions] [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75e12-109">Opis</span><span class="sxs-lookup"><span data-stu-id="75e12-109">DESCRIPTION</span></span>
<span data-ttu-id="75e12-110">Utwórz obraz rozszerzenia maszyny wirtualnej w programie Publisher i w wersji.</span><span class="sxs-lookup"><span data-stu-id="75e12-110">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="75e12-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="75e12-111">EXAMPLES</span></span>

### <span data-ttu-id="75e12-112">Przykład 1: Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="75e12-112">Example 1: Add-AzsVMExtension</span></span>
```powershell
PS C:\> Add-AzsVMExtension -Location "local" -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"

ExtensionType            : MicroExtension
TypeHandlerVersion       : 0.1.0
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/local/artifactTypes/VMExtension/publishers/Microsoft/types/MicroExtension/versions/0.1.0
IsSystemExtension        : False
Location                 : local
Name                     :
ProvisioningState        : Creating
Publisher                : Microsoft
SourceBlobUri            : https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip
SupportMultipleExtension : True
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Linux
```

<span data-ttu-id="75e12-113">Użyj linku publicznie dostępnego, aby podać lokalizację rozszerzenia lub identyfikator URI do obiektu blob platformy Azure przy użyciu SasUri.</span><span class="sxs-lookup"><span data-stu-id="75e12-113">Use a publicly accessible link to provide the location of the extension, or the URI to an Azure Blob using the SasUri.</span></span>

## <span data-ttu-id="75e12-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="75e12-114">PARAMETERS</span></span>

### <span data-ttu-id="75e12-115">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="75e12-115">-ComputeRole</span></span>
<span data-ttu-id="75e12-116">Rola obliczeniowa</span><span class="sxs-lookup"><span data-stu-id="75e12-116">Compute role</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75e12-117">-DefaultProfile</span></span>
<span data-ttu-id="75e12-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="75e12-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75e12-119">-Rozszerzenie</span><span class="sxs-lookup"><span data-stu-id="75e12-119">-Extension</span></span>
<span data-ttu-id="75e12-120">Parametry używane do tworzenia nowego obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75e12-120">Parameters used to create a new Virtual Machine Extension Image.</span></span>
<span data-ttu-id="75e12-121">Aby skonstruować, zobacz sekcję notatki dla właściwości rozszerzenia i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="75e12-121">To construct, see NOTES section for EXTENSION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="75e12-122">-InputObject</span></span>
<span data-ttu-id="75e12-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="75e12-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-124">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="75e12-124">-IsSystemExtension</span></span>
<span data-ttu-id="75e12-125">Wskazuje, czy rozszerzenie dotyczy systemu.</span><span class="sxs-lookup"><span data-stu-id="75e12-125">Indicates if the extension is for the system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="75e12-126">-Location</span></span>
<span data-ttu-id="75e12-127">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="75e12-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-128">-PropertiesPublisher</span><span class="sxs-lookup"><span data-stu-id="75e12-128">-PropertiesPublisher</span></span>
<span data-ttu-id="75e12-129">Wydawca rozszerzenia maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="75e12-129">The publisher of the VM Extension</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-130">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="75e12-130">-ProvisioningState</span></span>
<span data-ttu-id="75e12-131">Stan rozbudowy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="75e12-131">Provisioning state of extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-132">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="75e12-132">-Publisher</span></span>
<span data-ttu-id="75e12-133">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="75e12-133">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-134">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="75e12-134">-SourceBlob</span></span>
<span data-ttu-id="75e12-135">Identyfikator URI do obiektu blob platformy Azure lub AzureStack.</span><span class="sxs-lookup"><span data-stu-id="75e12-135">URI to Azure or AzureStack blob.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-136">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="75e12-136">-SubscriptionId</span></span>
<span data-ttu-id="75e12-137">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="75e12-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="75e12-138">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="75e12-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-139">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="75e12-139">-SupportMultipleExtensions</span></span>
<span data-ttu-id="75e12-140">Prawda, jeśli obsługuje wiele rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="75e12-140">True if supports multiple extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-141">-Type</span><span class="sxs-lookup"><span data-stu-id="75e12-141">-Type</span></span>
<span data-ttu-id="75e12-142">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="75e12-142">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-143">-Version</span><span class="sxs-lookup"><span data-stu-id="75e12-143">-Version</span></span>
<span data-ttu-id="75e12-144">Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="75e12-144">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-145">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="75e12-145">-VmOsType</span></span>
<span data-ttu-id="75e12-146">Docelowy typ systemu operacyjnego maszyny wirtualnej potrzebny do wdrożenia obsługi rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="75e12-146">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-147">-VMScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="75e12-147">-VMScaleSetEnabled</span></span>
<span data-ttu-id="75e12-148">Wartość wskazująca, czy rozszerzenie obsługuje funkcję skalowania skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75e12-148">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="75e12-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75e12-149">-Confirm</span></span>
<span data-ttu-id="75e12-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75e12-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75e12-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75e12-151">-WhatIf</span></span>
<span data-ttu-id="75e12-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75e12-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75e12-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="75e12-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75e12-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75e12-154">CommonParameters</span></span>
<span data-ttu-id="75e12-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75e12-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75e12-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75e12-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75e12-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75e12-157">INPUTS</span></span>

### <span data-ttu-id="75e12-158">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20151201Preview. IVMExtensionParameters</span><span class="sxs-lookup"><span data-stu-id="75e12-158">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters</span></span>

### <span data-ttu-id="75e12-159">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="75e12-159">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="75e12-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="75e12-160">OUTPUTS</span></span>

### <span data-ttu-id="75e12-161">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="75e12-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="75e12-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="75e12-162">NOTES</span></span>

<span data-ttu-id="75e12-163">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="75e12-163">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75e12-164">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="75e12-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="75e12-165">ROZSZERZENIE <IVMExtensionParameters> : parametry użyte do utworzenia nowego obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75e12-165">EXTENSION <IVMExtensionParameters>: Parameters used to create a new Virtual Machine Extension Image.</span></span>
  - <span data-ttu-id="75e12-166">`[ComputeRole <String>]`: Rola COMPUTE</span><span class="sxs-lookup"><span data-stu-id="75e12-166">`[ComputeRole <String>]`: Compute role</span></span>
  - <span data-ttu-id="75e12-167">`[IsSystemExtension <Boolean?>]`: Wskazuje, czy rozszerzenie dotyczy systemu.</span><span class="sxs-lookup"><span data-stu-id="75e12-167">`[IsSystemExtension <Boolean?>]`: Indicates if the extension is for the system.</span></span>
  - <span data-ttu-id="75e12-168">`[ProvisioningState <ProvisioningState?>]`: Stan rozbudowy rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="75e12-168">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of extension.</span></span>
  - <span data-ttu-id="75e12-169">`[Publisher <String>]`: Wydawca rozszerzenia maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="75e12-169">`[Publisher <String>]`: The publisher of the VM Extension</span></span>
  - <span data-ttu-id="75e12-170">`[SourceBlobUri <String>]`: Identyfikator URI na platformie Azure lub AzureStack BLOB.</span><span class="sxs-lookup"><span data-stu-id="75e12-170">`[SourceBlobUri <String>]`: URI to Azure or AzureStack blob.</span></span>
  - <span data-ttu-id="75e12-171">`[SupportMultipleExtension <Boolean?>]`: True (prawda), jeśli obsługuje wiele rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="75e12-171">`[SupportMultipleExtension <Boolean?>]`: True if supports multiple extensions.</span></span>
  - <span data-ttu-id="75e12-172">`[VMScaleSetEnabled <Boolean?>]`: Wartość wskazująca, czy rozszerzenie obsługuje funkcję skali maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="75e12-172">`[VMScaleSetEnabled <Boolean?>]`: Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>
  - <span data-ttu-id="75e12-173">`[VmosType <OSType?>]`: Docelowy typ systemu operacyjnego maszyny wirtualnej potrzebny do wdrożenia obsługi rozszerzeń.</span><span class="sxs-lookup"><span data-stu-id="75e12-173">`[VmosType <OSType?>]`: Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

<span data-ttu-id="75e12-174">INPUTobject <IComputeAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="75e12-174">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75e12-175">`[DiskId <String>]`: Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="75e12-175">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="75e12-176">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="75e12-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75e12-177">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="75e12-177">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="75e12-178">`[MigrationId <String>]`: Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="75e12-178">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="75e12-179">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="75e12-179">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="75e12-180">`[Publisher <String>]`: Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="75e12-180">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="75e12-181">`[QuotaName <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="75e12-181">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="75e12-182">`[Sku <String>]`: Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="75e12-182">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="75e12-183">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="75e12-183">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="75e12-184">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="75e12-184">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="75e12-185">`[Type <String>]`: Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="75e12-185">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="75e12-186">`[Version <String>]`: Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="75e12-186">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="75e12-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75e12-187">RELATED LINKS</span></span>

