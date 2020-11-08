---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232197"
---
# <span data-ttu-id="febd6-101">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="febd6-101">Get-AzManagedHsm</span></span>

## <span data-ttu-id="febd6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="febd6-102">SYNOPSIS</span></span>
<span data-ttu-id="febd6-103">Pobierz HSMs zarządzaną.</span><span class="sxs-lookup"><span data-stu-id="febd6-103">Get managed HSMs.</span></span>

## <span data-ttu-id="febd6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="febd6-104">SYNTAX</span></span>

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="febd6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="febd6-105">DESCRIPTION</span></span>
<span data-ttu-id="febd6-106">Polecenie cmdlet **Get-AzManagedHsm** pobiera informacje o HSMsie zarządzanym w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="febd6-106">The **Get-AzManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="febd6-107">Wszystkie zarządzane wystąpienia HSMs można wyświetlać w ramach abonamentu lub filtrować wyniki według grupy zasobów lub określonego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="febd6-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="febd6-108">Należy zauważyć, że chociaż określenie grupy zasobów jest opcjonalne dla tego polecenia cmdlet, gdy jest wyświetlany jeden zarządzany obiekt HSM, należy to zrobić w celu uzyskania lepszej wydajności.</span><span class="sxs-lookup"><span data-stu-id="febd6-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="febd6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="febd6-109">EXAMPLES</span></span>

### <span data-ttu-id="febd6-110">Przykład 1: uzyskiwanie wszystkich zarządzanych HSMs w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="febd6-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="febd6-111">To polecenie pobiera wszystkie HSMs zarządzane w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="febd6-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="febd6-112">Przykład 2: uzyskiwanie określonego zarządzanego modułu HSM</span><span class="sxs-lookup"><span data-stu-id="febd6-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="febd6-113">To polecenie umożliwia pobieranie zarządzanego modułu HSM o nazwie myhsm w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="febd6-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="febd6-114">Przykład 3: uzyskiwanie zarządzanych HSMs w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="febd6-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="febd6-115">To polecenie pobiera wszystkie HSMs zarządzane w grupie zasobów o nazwie myrg1.</span><span class="sxs-lookup"><span data-stu-id="febd6-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="febd6-116">Przykład 4: uzyskiwanie HSMs zarządzanych przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="febd6-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="febd6-117">To polecenie uzyskuje wszystkie HSMs zarządzane w subskrypcji rozpoczynające się od "myhsm".</span><span class="sxs-lookup"><span data-stu-id="febd6-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="febd6-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="febd6-118">PARAMETERS</span></span>

### <span data-ttu-id="febd6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="febd6-119">-DefaultProfile</span></span>
<span data-ttu-id="febd6-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="febd6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="febd6-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="febd6-121">-Name</span></span>
<span data-ttu-id="febd6-122">Nazwa modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="febd6-122">HSM name.</span></span> <span data-ttu-id="febd6-123">Polecenie cmdlet tworzy nazwę FQDN modułu HSM na podstawie nazwy i obecnie wybranego środowiska.</span><span class="sxs-lookup"><span data-stu-id="febd6-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febd6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="febd6-124">-ResourceGroupName</span></span>
<span data-ttu-id="febd6-125">Określa nazwę grupy zasobów skojarzonej z badanym zarządzanym HSM.</span><span class="sxs-lookup"><span data-stu-id="febd6-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="febd6-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="febd6-126">-Tag</span></span>
<span data-ttu-id="febd6-127">Określa klucz i opcjonalną wartość określonego tagu w celu filtrowania listy zarządzanych HSMs według.</span><span class="sxs-lookup"><span data-stu-id="febd6-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="febd6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febd6-128">CommonParameters</span></span>
<span data-ttu-id="febd6-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="febd6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febd6-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="febd6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febd6-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="febd6-131">INPUTS</span></span>

### <span data-ttu-id="febd6-132">System. String</span><span class="sxs-lookup"><span data-stu-id="febd6-132">System.String</span></span>

### <span data-ttu-id="febd6-133">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="febd6-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="febd6-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="febd6-134">OUTPUTS</span></span>

### <span data-ttu-id="febd6-135">Microsoft. Azure. Commands. platforming. models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="febd6-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="febd6-136">Microsoft. Azure. Commands. platforming. models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="febd6-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="febd6-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="febd6-137">NOTES</span></span>

## <span data-ttu-id="febd6-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="febd6-138">RELATED LINKS</span></span>

[<span data-ttu-id="febd6-139">Nowe — AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="febd6-139">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="febd6-140">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="febd6-140">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="febd6-141">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="febd6-141">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)