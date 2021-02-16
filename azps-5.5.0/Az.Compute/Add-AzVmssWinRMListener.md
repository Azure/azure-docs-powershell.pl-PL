---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 471baa126cd58bb241fa6b8da358769d09be3f20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195082"
---
# <span data-ttu-id="e2856-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="e2856-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="e2856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2856-102">SYNOPSIS</span></span>
<span data-ttu-id="e2856-103">Dodaje słuchacza usługi WinRM do usługi MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="e2856-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="e2856-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e2856-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2856-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e2856-105">DESCRIPTION</span></span>
<span data-ttu-id="e2856-106">Polecenie **cmdlet Add-AzVmssWinRMListener** dodaje słuchacza usługi Windows Remote Management (WinRM) w zestawie skal maszyn wirtualnych (VIRTUAL Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="e2856-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e2856-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e2856-107">EXAMPLES</span></span>

### <span data-ttu-id="e2856-108">Przykład 1. Dodawanie słuchacza usługi WinRM do usługi MASZYNY WIRTUALNE</span><span class="sxs-lookup"><span data-stu-id="e2856-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="e2856-109">W tym przykładzie dodano słuchacza usługi WinRM do usługi MASZYNY WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="e2856-109">This example adds a WinRM listener to the VMSS.</span></span>
<span data-ttu-id="e2856-110">Pierwsze polecenie tworzy obiekt konfiguracji maszyny WIRTUALNEJ za pomocą polecenia cmdlet **New-AzVmssConfig** i zapisuje wynik w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="e2856-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="e2856-111">Drugie polecenie dodaje słuchacza usługi WinRM protokołu HTTP z certyfikatem o określonym adresie URL do usługi MASZYNY WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="e2856-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="e2856-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2856-112">PARAMETERS</span></span>

### <span data-ttu-id="e2856-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="e2856-113">-CertificateUrl</span></span>
<span data-ttu-id="e2856-114">Określa link (jako adres URL) certyfikatu, za pomocą którego są aprowowane nowe maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="e2856-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="e2856-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2856-115">-DefaultProfile</span></span>
<span data-ttu-id="e2856-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2856-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2856-117">— Protokół</span><span class="sxs-lookup"><span data-stu-id="e2856-117">-Protocol</span></span>
<span data-ttu-id="e2856-118">Określa protokół odbiorcy usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="e2856-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="e2856-119">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e2856-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e2856-120">Http</span><span class="sxs-lookup"><span data-stu-id="e2856-120">Http</span></span>
- <span data-ttu-id="e2856-121">https</span><span class="sxs-lookup"><span data-stu-id="e2856-121">Https</span></span>

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

### <span data-ttu-id="e2856-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e2856-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e2856-123">Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="e2856-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="e2856-124">Aby utworzyć obiekt, New-AzVmssConfig użyć polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2856-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="e2856-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2856-125">-Confirm</span></span>
<span data-ttu-id="e2856-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e2856-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2856-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2856-127">-WhatIf</span></span>
<span data-ttu-id="e2856-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2856-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2856-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e2856-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2856-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2856-130">CommonParameters</span></span>
<span data-ttu-id="e2856-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2856-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2856-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2856-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2856-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2856-133">INPUTS</span></span>

### <span data-ttu-id="e2856-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e2856-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e2856-135">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="e2856-135">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ProtocolTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="e2856-136">System.String</span><span class="sxs-lookup"><span data-stu-id="e2856-136">System.String</span></span>

## <span data-ttu-id="e2856-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e2856-137">OUTPUTS</span></span>

### <span data-ttu-id="e2856-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e2856-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e2856-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e2856-139">NOTES</span></span>

## <span data-ttu-id="e2856-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2856-140">RELATED LINKS</span></span>

[<span data-ttu-id="e2856-141">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e2856-141">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


