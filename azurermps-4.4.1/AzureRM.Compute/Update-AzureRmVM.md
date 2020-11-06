---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: ad337c07f22b2805002347758f91bf0ea781adad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548331"
---
# <span data-ttu-id="39f09-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39f09-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="39f09-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39f09-102">SYNOPSIS</span></span>
<span data-ttu-id="39f09-103">Umożliwia zaktualizowanie stanu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="39f09-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39f09-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39f09-104">SYNTAX</span></span>

### <span data-ttu-id="39f09-105">ResourceGroupNameParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="39f09-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39f09-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="39f09-106">IdParameterSetName</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39f09-107">Opis</span><span class="sxs-lookup"><span data-stu-id="39f09-107">DESCRIPTION</span></span>
<span data-ttu-id="39f09-108">Polecenie cmdlet **Update-AzureRmVM** powoduje zaktualizowanie stanu maszyny wirtualnej platformy Azure do stanu obiektu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39f09-108">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="39f09-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39f09-109">EXAMPLES</span></span>

### <span data-ttu-id="39f09-110">Przykład 1: aktualizowanie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="39f09-110">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="39f09-111">To polecenie powoduje zaktualizowanie maszyny wirtualnej $VirtualMachine w programie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="39f09-111">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="39f09-112">Polecenie aktualizuje je za pomocą obiektu maszyny wirtualnej przechowywanego w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="39f09-112">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="39f09-113">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="39f09-113">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="39f09-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39f09-114">PARAMETERS</span></span>

### <span data-ttu-id="39f09-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="39f09-115">-AssignIdentity</span></span>
<span data-ttu-id="39f09-116">Określ tożsamość przypisaną systemowi dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39f09-116">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f09-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39f09-117">-DefaultProfile</span></span>
<span data-ttu-id="39f09-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39f09-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f09-119">-ID</span><span class="sxs-lookup"><span data-stu-id="39f09-119">-Id</span></span>
<span data-ttu-id="39f09-120">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39f09-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f09-121">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="39f09-121">-IdentityType</span></span>
<span data-ttu-id="39f09-122">Typ tożsamości używanej dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39f09-122">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="39f09-123">Obecnie jedynym obsługiwanym typem jest SystemAssigned ', co powoduje niejawne utworzenie tożsamości.</span><span class="sxs-lookup"><span data-stu-id="39f09-123">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f09-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39f09-124">-ResourceGroupName</span></span>
<span data-ttu-id="39f09-125">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39f09-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39f09-126">-Tagi</span><span class="sxs-lookup"><span data-stu-id="39f09-126">-Tags</span></span>
<span data-ttu-id="39f09-127">Określa zasoby i grupy zasobów, które można wyznacznikować za pomocą zestawu par nazwa-wartość.</span><span class="sxs-lookup"><span data-stu-id="39f09-127">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="39f09-128">Dodawanie znaczników do zasobów umożliwia grupowanie zasobów między grupami zasobów i tworzenie własnych widoków.</span><span class="sxs-lookup"><span data-stu-id="39f09-128">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="39f09-129">Każdy zasób lub Grupa zasobów może zawierać maksymalnie 15 tagów.</span><span class="sxs-lookup"><span data-stu-id="39f09-129">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="39f09-130">-VM</span><span class="sxs-lookup"><span data-stu-id="39f09-130">-VM</span></span>
<span data-ttu-id="39f09-131">Określa obiekt lokalnego maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39f09-131">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="39f09-132">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="39f09-132">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="39f09-133">Ten obiekt maszyny wirtualnej zawiera zaktualizowany stan maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="39f09-133">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39f09-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="39f09-134">-Confirm</span></span>
<span data-ttu-id="39f09-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f09-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f09-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39f09-136">-WhatIf</span></span>
<span data-ttu-id="39f09-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39f09-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="39f09-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="39f09-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39f09-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39f09-139">CommonParameters</span></span>
<span data-ttu-id="39f09-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39f09-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39f09-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39f09-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39f09-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39f09-142">INPUTS</span></span>

## <span data-ttu-id="39f09-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39f09-143">OUTPUTS</span></span>

## <span data-ttu-id="39f09-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39f09-144">NOTES</span></span>

## <span data-ttu-id="39f09-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39f09-145">RELATED LINKS</span></span>

[<span data-ttu-id="39f09-146">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39f09-146">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="39f09-147">Nowe — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39f09-147">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="39f09-148">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39f09-148">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="39f09-149">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39f09-149">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="39f09-150">Start — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39f09-150">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="39f09-151">Zatrzymaj — AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="39f09-151">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="39f09-152">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="39f09-152">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


