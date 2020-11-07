---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 79d6a48ca2c6f86b84e8f02514191a2e4815f350
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706465"
---
# <span data-ttu-id="d4a8a-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="d4a8a-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="d4a8a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4a8a-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a8a-103">Dodaje odbiornik usługi WinRM do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="d4a8a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4a8a-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4a8a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d4a8a-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a8a-106">Polecenie cmdlet **Add-AzVmssWinRMListener** umożliwia dodanie odbiornika zdalnego zarządzania systemem Windows (WinRM) na zestawie skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d4a8a-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d4a8a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4a8a-107">EXAMPLES</span></span>

### <span data-ttu-id="d4a8a-108">Przykład 1: Dodawanie odbiornika usługi WinRM do VMSS</span><span class="sxs-lookup"><span data-stu-id="d4a8a-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="d4a8a-109">W tym przykładzie dodano odbiornik usługi WinRM do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="d4a8a-110">W pierwszym poleceniu użyto polecenia cmdlet **New-AzVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="d4a8a-111">Drugie polecenie dodaje odbiornik protokołu HTTP o usłudze WinRM z certyfikatem pod określonym adresem URL do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="d4a8a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4a8a-112">PARAMETERS</span></span>

### <span data-ttu-id="d4a8a-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="d4a8a-113">-CertificateUrl</span></span>
<span data-ttu-id="d4a8a-114">Określa łącze (jako adres URL) certyfikatu, z którym Zainicjowano obsługę administracyjną nowych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a8a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a8a-115">-DefaultProfile</span></span>
<span data-ttu-id="d4a8a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4a8a-117">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="d4a8a-117">-Protocol</span></span>
<span data-ttu-id="d4a8a-118">Określa protokół odbiornika usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="d4a8a-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d4a8a-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d4a8a-120">URL</span><span class="sxs-lookup"><span data-stu-id="d4a8a-120">Http</span></span>
- <span data-ttu-id="d4a8a-121">Https</span><span class="sxs-lookup"><span data-stu-id="d4a8a-121">Https</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ProtocolTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a8a-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d4a8a-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d4a8a-123">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="d4a8a-124">Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a8a-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4a8a-125">-Confirm</span></span>
<span data-ttu-id="d4a8a-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a8a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a8a-127">-WhatIf</span></span>
<span data-ttu-id="d4a8a-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4a8a-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a8a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a8a-130">CommonParameters</span></span>
<span data-ttu-id="d4a8a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a8a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a8a-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4a8a-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a8a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4a8a-133">INPUTS</span></span>

### <span data-ttu-id="d4a8a-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d4a8a-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d4a8a-135">System. Nullable "1 [[Microsoft. Azure. Management. COMPUTE. models. ProtocolTypes, Microsoft. Azure. Management. Framework</span><span class="sxs-lookup"><span data-stu-id="d4a8a-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d4a8a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d4a8a-136">System.String</span></span>

## <span data-ttu-id="d4a8a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4a8a-137">OUTPUTS</span></span>

### <span data-ttu-id="d4a8a-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d4a8a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d4a8a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4a8a-139">NOTES</span></span>

## <span data-ttu-id="d4a8a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4a8a-140">RELATED LINKS</span></span>

[<span data-ttu-id="d4a8a-141">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d4a8a-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)

