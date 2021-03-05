---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: b65fed5670f34072504c736283ba12e51086d3d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995478"
---
# <span data-ttu-id="4866c-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4866c-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="4866c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4866c-102">SYNOPSIS</span></span>
<span data-ttu-id="4866c-103">Uzyskiwanie zarządzanych hsm.</span><span class="sxs-lookup"><span data-stu-id="4866c-103">Get managed HSMs.</span></span>

## <span data-ttu-id="4866c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4866c-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4866c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4866c-105">DESCRIPTION</span></span>
<span data-ttu-id="4866c-106">Polecenie **cmdlet Get-AzKeyVaultManagedHsm** pobiera informacje o zarządzanych modułach HSM w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4866c-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="4866c-107">Można wyświetlić wszystkie zarządzane wystąpienia HSM w subskrypcji lub przefiltrować wyniki według grupy zasobów lub określonego zarządzanego modułu hsm.</span><span class="sxs-lookup"><span data-stu-id="4866c-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="4866c-108">Pamiętaj, że mimo że określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet w przypadku uzyskania pojedynczego zarządzanego modułu HSM, należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="4866c-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="4866c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4866c-109">EXAMPLES</span></span>

### <span data-ttu-id="4866c-110">Przykład 1. Uzyskiwanie wszystkich zarządzanych kodów HSM w ramach bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4866c-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="4866c-111">To polecenie pobiera wszystkie zarządzane moduły HSM w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4866c-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="4866c-112">Przykład 2. Uzyskiwanie określonego zarządzanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="4866c-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="4866c-113">To polecenie pobiera zarządzany moduł HSM o nazwie myhsm w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4866c-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="4866c-114">Przykład 3. Uzyskiwanie zarządzanych hsm w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="4866c-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="4866c-115">To polecenie pobiera wszystkie zarządzane moduły HSM w grupie zasobów o nazwie myrg1.</span><span class="sxs-lookup"><span data-stu-id="4866c-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="4866c-116">Przykład 4. Uzyskiwanie zarządzanych hsm przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="4866c-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="4866c-117">To polecenie pobiera wszystkie zarządzane moduły HSM w subskrypcji, które zaczynają się od "myhsm".</span><span class="sxs-lookup"><span data-stu-id="4866c-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="4866c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4866c-118">PARAMETERS</span></span>

### <span data-ttu-id="4866c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4866c-119">-DefaultProfile</span></span>
<span data-ttu-id="4866c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4866c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4866c-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4866c-121">-Name</span></span>
<span data-ttu-id="4866c-122">Nazwa HSM.</span><span class="sxs-lookup"><span data-stu-id="4866c-122">HSM name.</span></span> <span data-ttu-id="4866c-123">Polecenie cmdlet tworzy nazwę FQDN modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="4866c-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4866c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4866c-124">-ResourceGroupName</span></span>
<span data-ttu-id="4866c-125">Określa nazwę grupy zasobów skojarzonej z zarządzanym modułem HSM, do których jest pytany.</span><span class="sxs-lookup"><span data-stu-id="4866c-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4866c-126">— Tag</span><span class="sxs-lookup"><span data-stu-id="4866c-126">-Tag</span></span>
<span data-ttu-id="4866c-127">Określa klucz i opcjonalną wartość określonego tagu, według których ma być filtrowana lista zarządzanych hsM.</span><span class="sxs-lookup"><span data-stu-id="4866c-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4866c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4866c-128">CommonParameters</span></span>
<span data-ttu-id="4866c-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4866c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4866c-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4866c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4866c-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4866c-131">INPUTS</span></span>

### <span data-ttu-id="4866c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4866c-132">System.String</span></span>

### <span data-ttu-id="4866c-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4866c-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4866c-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4866c-134">OUTPUTS</span></span>

### <span data-ttu-id="4866c-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4866c-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="4866c-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4866c-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="4866c-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4866c-137">NOTES</span></span>

## <span data-ttu-id="4866c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4866c-138">RELATED LINKS</span></span>

[<span data-ttu-id="4866c-139">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4866c-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="4866c-140">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4866c-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="4866c-141">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4866c-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)