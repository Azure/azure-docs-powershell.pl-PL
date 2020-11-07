---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: e10e60845c9aeb90b7c708a65f7d681d9894b022
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706342"
---
# <span data-ttu-id="f9b96-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="f9b96-101">New-AzHost</span></span>

## <span data-ttu-id="f9b96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9b96-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b96-103">Umożliwia utworzenie hosta.</span><span class="sxs-lookup"><span data-stu-id="f9b96-103">Creates a  host.</span></span>

## <span data-ttu-id="f9b96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9b96-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9b96-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9b96-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b96-106">To polecenie cmdlet utworzy hosta.</span><span class="sxs-lookup"><span data-stu-id="f9b96-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="f9b96-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9b96-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b96-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9b96-108">Example 1</span></span>
```
PS C:\> New-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName -Location $location -Sku $skuName

ResourceGroupName    : myrg01
PlatformFaultDomain  : 0
AutoReplaceOnFailure : True
HostId               : 00000000-0000-0000-0000-000000000000
ProvisioningTime     : 7/25/2019 8:34:16 PM
ProvisioningState    : Succeeded
Sku                  : 
  Name               : ESv3-Type1
Id                   : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myrg01/providers/Microsoft.Compute/hostGroups/myhostgroup01/hosts/myhost01
Name                 : myhost01
Location             : eastus
Tags                 : {"key1":"val2"}
```

<span data-ttu-id="f9b96-109">To polecenie tworzy Host danej jednostki SKU w danej grupie hostów i określoną lokalizację.</span><span class="sxs-lookup"><span data-stu-id="f9b96-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="f9b96-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9b96-110">PARAMETERS</span></span>

### <span data-ttu-id="f9b96-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9b96-111">-AsJob</span></span>
<span data-ttu-id="f9b96-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f9b96-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9b96-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="f9b96-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="f9b96-114">Określa, czy host powinien być zastępowany automatycznie w przypadku niepowodzenia.</span><span class="sxs-lookup"><span data-stu-id="f9b96-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="f9b96-115">Wartość jest domyślnie równa "prawda", gdy nie jest podana.</span><span class="sxs-lookup"><span data-stu-id="f9b96-115">The value is defaulted to 'true' when not provided.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b96-116">-DefaultProfile</span></span>
<span data-ttu-id="f9b96-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b96-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9b96-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b96-118">-HostGroupName</span></span>
<span data-ttu-id="f9b96-119">Określa nazwę grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="f9b96-119">Specifies the name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b96-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f9b96-120">-LicenseType</span></span>
<span data-ttu-id="f9b96-121">Określa typ licencji na oprogramowanie, który zostanie zastosowany do maszyn wirtualnych wdrożonych na hoście.</span><span class="sxs-lookup"><span data-stu-id="f9b96-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="f9b96-122">Możliwe wartości: brak, Windows_Server_Hybrid i Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="f9b96-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="f9b96-123">Wartość domyślna to None.</span><span class="sxs-lookup"><span data-stu-id="f9b96-123">Default value is None.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.DedicatedHostLicenseTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, WindowsServerHybrid, WindowsServerPerpetual

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b96-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f9b96-124">-Location</span></span>
<span data-ttu-id="f9b96-125">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="f9b96-125">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b96-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9b96-126">-Name</span></span>
<span data-ttu-id="f9b96-127">Określa nazwę hosta.</span><span class="sxs-lookup"><span data-stu-id="f9b96-127">Specifies the name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b96-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="f9b96-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="f9b96-129">Określa liczbę domen błędów platformy hosta.</span><span class="sxs-lookup"><span data-stu-id="f9b96-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="f9b96-130">Wartość minimalna wynosi 0, a wartość maksymalna to 2.</span><span class="sxs-lookup"><span data-stu-id="f9b96-130">Then minimum value is 0 and the maximum value is 2.</span></span>

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

### <span data-ttu-id="f9b96-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b96-131">-ResourceGroupName</span></span>
<span data-ttu-id="f9b96-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9b96-132">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9b96-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="f9b96-133">-Sku</span></span>
<span data-ttu-id="f9b96-134">Określa nazwę jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="f9b96-134">Specifies the name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b96-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9b96-135">-Tag</span></span>
<span data-ttu-id="f9b96-136">Określa znaczniki.</span><span class="sxs-lookup"><span data-stu-id="f9b96-136">Specifies Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9b96-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9b96-137">-Confirm</span></span>
<span data-ttu-id="f9b96-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9b96-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b96-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b96-139">-WhatIf</span></span>
<span data-ttu-id="f9b96-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9b96-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9b96-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f9b96-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b96-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b96-142">CommonParameters</span></span>
<span data-ttu-id="f9b96-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9b96-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b96-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9b96-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b96-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9b96-145">INPUTS</span></span>

### <span data-ttu-id="f9b96-146">System. String</span><span class="sxs-lookup"><span data-stu-id="f9b96-146">System.String</span></span>

## <span data-ttu-id="f9b96-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9b96-147">OUTPUTS</span></span>

### <span data-ttu-id="f9b96-148">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSHost</span><span class="sxs-lookup"><span data-stu-id="f9b96-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="f9b96-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9b96-149">NOTES</span></span>

## <span data-ttu-id="f9b96-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9b96-150">RELATED LINKS</span></span>
