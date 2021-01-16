---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8d602e5cbb3a24307ba77daf9a88a79a3c5bb705
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333034"
---
# <span data-ttu-id="1fdca-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1fdca-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="1fdca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fdca-102">SYNOPSIS</span></span>
<span data-ttu-id="1fdca-103">Pobierz HSMs zarządzaną.</span><span class="sxs-lookup"><span data-stu-id="1fdca-103">Get managed HSMs.</span></span>

## <span data-ttu-id="1fdca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fdca-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fdca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1fdca-105">DESCRIPTION</span></span>
<span data-ttu-id="1fdca-106">Polecenie cmdlet **Get-AzKeyVaultManagedHsm** pobiera informacje o HSMsie zarządzanym w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="1fdca-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="1fdca-107">Wszystkie zarządzane wystąpienia HSMs można wyświetlać w ramach abonamentu lub filtrować wyniki według grupy zasobów lub określonego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="1fdca-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="1fdca-108">Należy zauważyć, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, gdy jest wyświetlany jeden zarządzany obiekt HSM, należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="1fdca-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="1fdca-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fdca-109">EXAMPLES</span></span>

### <span data-ttu-id="1fdca-110">Przykład 1: uzyskiwanie wszystkich zarządzanych HSMs w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1fdca-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="1fdca-111">To polecenie pobiera wszystkie HSMs zarządzane w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1fdca-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="1fdca-112">Przykład 2: uzyskiwanie określonego zarządzanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="1fdca-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="1fdca-113">To polecenie umożliwia pobieranie zarządzanego modułu HSM o nazwie myhsm w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1fdca-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="1fdca-114">Przykład 3: uzyskiwanie zarządzanych HSMs w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="1fdca-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="1fdca-115">To polecenie pobiera wszystkie HSMs zarządzane w grupie zasobów o nazwie myrg1.</span><span class="sxs-lookup"><span data-stu-id="1fdca-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="1fdca-116">Przykład 4: uzyskiwanie HSMs zarządzanych przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="1fdca-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="1fdca-117">To polecenie uzyskuje wszystkie HSMs zarządzane w subskrypcji rozpoczynające się od "myhsm".</span><span class="sxs-lookup"><span data-stu-id="1fdca-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="1fdca-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fdca-118">PARAMETERS</span></span>

### <span data-ttu-id="1fdca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fdca-119">-DefaultProfile</span></span>
<span data-ttu-id="1fdca-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fdca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fdca-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1fdca-121">-Name</span></span>
<span data-ttu-id="1fdca-122">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="1fdca-122">HSM name.</span></span> <span data-ttu-id="1fdca-123">Polecenie cmdlet tworzy nazwę FQDN modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="1fdca-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="1fdca-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fdca-124">-ResourceGroupName</span></span>
<span data-ttu-id="1fdca-125">Określa nazwę grupy zasobów skojarzonej z badanym zarządzanym HSM.</span><span class="sxs-lookup"><span data-stu-id="1fdca-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

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

### <span data-ttu-id="1fdca-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="1fdca-126">-Tag</span></span>
<span data-ttu-id="1fdca-127">Określa klucz i opcjonalną wartość określonego tagu w celu filtrowania listy zarządzanych HSMs według.</span><span class="sxs-lookup"><span data-stu-id="1fdca-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="1fdca-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fdca-128">CommonParameters</span></span>
<span data-ttu-id="1fdca-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fdca-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fdca-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fdca-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fdca-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fdca-131">INPUTS</span></span>

### <span data-ttu-id="1fdca-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1fdca-132">System.String</span></span>

### <span data-ttu-id="1fdca-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1fdca-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1fdca-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fdca-134">OUTPUTS</span></span>

### <span data-ttu-id="1fdca-135">Microsoft. Azure. Commands. platforming. models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1fdca-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="1fdca-136">Microsoft. Azure. Commands. platforming. models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1fdca-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="1fdca-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fdca-137">NOTES</span></span>

## <span data-ttu-id="1fdca-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fdca-138">RELATED LINKS</span></span>

[<span data-ttu-id="1fdca-139">Nowe — AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1fdca-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="1fdca-140">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1fdca-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="1fdca-141">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="1fdca-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)