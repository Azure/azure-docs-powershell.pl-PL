---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzHost.md
ms.openlocfilehash: adeee59745aa3f14fe3b5580139b17412e496f0f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959681"
---
# <span data-ttu-id="33916-101">New-AzHost</span><span class="sxs-lookup"><span data-stu-id="33916-101">New-AzHost</span></span>

## <span data-ttu-id="33916-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33916-102">SYNOPSIS</span></span>
<span data-ttu-id="33916-103">Tworzy hosta.</span><span class="sxs-lookup"><span data-stu-id="33916-103">Creates a  host.</span></span>

## <span data-ttu-id="33916-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="33916-104">SYNTAX</span></span>

```
New-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-Location] <String>
 -Sku <String> [-PlatformFaultDomain <Int32>] [-AutoReplaceOnFailure <Boolean>]
 [-LicenseType <DedicatedHostLicenseTypes>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33916-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="33916-105">DESCRIPTION</span></span>
<span data-ttu-id="33916-106">To polecenie cmdlet utworzy hosta.</span><span class="sxs-lookup"><span data-stu-id="33916-106">This cmdlet will create a Host.</span></span>

## <span data-ttu-id="33916-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="33916-107">EXAMPLES</span></span>

### <span data-ttu-id="33916-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33916-108">Example 1</span></span>
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

<span data-ttu-id="33916-109">To polecenie tworzy hosta danej sku w danej grupie hosta i danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="33916-109">This command creates a host of the given Sku in the given host group and the given location.</span></span>

## <span data-ttu-id="33916-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33916-110">PARAMETERS</span></span>

### <span data-ttu-id="33916-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="33916-111">-AsJob</span></span>
<span data-ttu-id="33916-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="33916-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33916-113">-AutoReplaceOnFailure</span><span class="sxs-lookup"><span data-stu-id="33916-113">-AutoReplaceOnFailure</span></span>
<span data-ttu-id="33916-114">Określa, czy w przypadku niepowodzenia host ma być automatycznie zamieniany.</span><span class="sxs-lookup"><span data-stu-id="33916-114">Specifies whether the host should be replaced automatically in case of a failure.</span></span> <span data-ttu-id="33916-115">Wartość domyślna to "true", jeśli nie jest podana.</span><span class="sxs-lookup"><span data-stu-id="33916-115">The value is defaulted to 'true' when not provided.</span></span>

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

### <span data-ttu-id="33916-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33916-116">-DefaultProfile</span></span>
<span data-ttu-id="33916-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="33916-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33916-118">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="33916-118">-HostGroupName</span></span>
<span data-ttu-id="33916-119">Określa nazwę grupy hostów.</span><span class="sxs-lookup"><span data-stu-id="33916-119">Specifies the name of the host group.</span></span>

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

### <span data-ttu-id="33916-120">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="33916-120">-LicenseType</span></span>
<span data-ttu-id="33916-121">Określa typ licencji oprogramowania, który będzie stosowany do maszyn wirtualnych wdrożonych na hoście.</span><span class="sxs-lookup"><span data-stu-id="33916-121">Specifies the software license type that will be applied to the VMs deployed on the host.</span></span> <span data-ttu-id="33916-122">Dopuszczalne wartości to: Brak, Windows_Server_Hybrid i Windows_Server_Perpetual.</span><span class="sxs-lookup"><span data-stu-id="33916-122">Possible values are: None, Windows_Server_Hybrid, and Windows_Server_Perpetual.</span></span>  <span data-ttu-id="33916-123">Wartość domyślna to Brak.</span><span class="sxs-lookup"><span data-stu-id="33916-123">Default value is None.</span></span>

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

### <span data-ttu-id="33916-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="33916-124">-Location</span></span>
<span data-ttu-id="33916-125">Określa lokalizację.</span><span class="sxs-lookup"><span data-stu-id="33916-125">Specifies the location.</span></span>

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

### <span data-ttu-id="33916-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="33916-126">-Name</span></span>
<span data-ttu-id="33916-127">Określa nazwę hosta.</span><span class="sxs-lookup"><span data-stu-id="33916-127">Specifies the name of the host.</span></span>

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

### <span data-ttu-id="33916-128">-PlatformFaultDomain</span><span class="sxs-lookup"><span data-stu-id="33916-128">-PlatformFaultDomain</span></span>
<span data-ttu-id="33916-129">Określa liczbę domeny błędu platformy hosta.</span><span class="sxs-lookup"><span data-stu-id="33916-129">Specifies the number of platform fault domain of the host.</span></span>  <span data-ttu-id="33916-130">Następnie wartość minimalna wynosi 0, a maksymalna 2.</span><span class="sxs-lookup"><span data-stu-id="33916-130">Then minimum value is 0 and the maximum value is 2.</span></span>

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

### <span data-ttu-id="33916-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33916-131">-ResourceGroupName</span></span>
<span data-ttu-id="33916-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="33916-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="33916-133">- SKU</span><span class="sxs-lookup"><span data-stu-id="33916-133">-Sku</span></span>
<span data-ttu-id="33916-134">Określa nazwę sku.</span><span class="sxs-lookup"><span data-stu-id="33916-134">Specifies the name of the SKU.</span></span>

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

### <span data-ttu-id="33916-135">— Tag</span><span class="sxs-lookup"><span data-stu-id="33916-135">-Tag</span></span>
<span data-ttu-id="33916-136">Określa tagi.</span><span class="sxs-lookup"><span data-stu-id="33916-136">Specifies Tags.</span></span>

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

### <span data-ttu-id="33916-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33916-137">-Confirm</span></span>
<span data-ttu-id="33916-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="33916-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33916-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33916-139">-WhatIf</span></span>
<span data-ttu-id="33916-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33916-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33916-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="33916-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33916-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33916-142">CommonParameters</span></span>
<span data-ttu-id="33916-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33916-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33916-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33916-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33916-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33916-145">INPUTS</span></span>

### <span data-ttu-id="33916-146">System.String</span><span class="sxs-lookup"><span data-stu-id="33916-146">System.String</span></span>

## <span data-ttu-id="33916-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33916-147">OUTPUTS</span></span>

### <span data-ttu-id="33916-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="33916-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="33916-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="33916-149">NOTES</span></span>

## <span data-ttu-id="33916-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33916-150">RELATED LINKS</span></span>
