---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsswinrmlistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssWinRMListener.md
ms.openlocfilehash: 00e61142948e42310dbd5c0be56660c17ec7e8e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893857"
---
# <span data-ttu-id="0e1e2-101">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="0e1e2-101">Add-AzVmssWinRMListener</span></span>

## <span data-ttu-id="0e1e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e1e2-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1e2-103">Dodaje odbiornik usługi WinRM do VMSS.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-103">Adds a WinRM listener to the VMSS.</span></span>

## <span data-ttu-id="0e1e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e1e2-104">SYNTAX</span></span>

```
Add-AzVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e1e2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e1e2-105">DESCRIPTION</span></span>
<span data-ttu-id="0e1e2-106">Polecenie cmdlet **Add-AzVmssWinRMListener** umożliwia dodanie odbiornika zdalnego zarządzania systemem Windows (WinRM) na zestawie skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0e1e2-106">The **Add-AzVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="0e1e2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e1e2-107">EXAMPLES</span></span>

### <span data-ttu-id="0e1e2-108">Przykład 1: Dodawanie odbiornika usługi WinRM do VMSS</span><span class="sxs-lookup"><span data-stu-id="0e1e2-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="0e1e2-109">W tym przykładzie dodano odbiornik usługi WinRM do VMSS.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="0e1e2-110">W pierwszym poleceniu użyto polecenia cmdlet **New-AzVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="0e1e2-111">Drugie polecenie dodaje odbiornik protokołu HTTP o usłudze WinRM z certyfikatem pod określonym adresem URL do VMSS.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="0e1e2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e1e2-112">PARAMETERS</span></span>

### <span data-ttu-id="0e1e2-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="0e1e2-113">-CertificateUrl</span></span>
<span data-ttu-id="0e1e2-114">Określa łącze (jako adres URL) certyfikatu, z którym Zainicjowano obsługę administracyjną nowych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e1e2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e1e2-115">-DefaultProfile</span></span>
<span data-ttu-id="0e1e2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e1e2-117">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="0e1e2-117">-Protocol</span></span>
<span data-ttu-id="0e1e2-118">Określa protokół odbiornika usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="0e1e2-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0e1e2-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0e1e2-120">URL</span><span class="sxs-lookup"><span data-stu-id="0e1e2-120">Http</span></span>
- <span data-ttu-id="0e1e2-121">Https</span><span class="sxs-lookup"><span data-stu-id="0e1e2-121">Https</span></span>

```yaml
Type: ProtocolTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e1e2-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0e1e2-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0e1e2-123">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="0e1e2-124">Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-124">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e1e2-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e1e2-125">-Confirm</span></span>
<span data-ttu-id="0e1e2-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e1e2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e1e2-127">-WhatIf</span></span>
<span data-ttu-id="0e1e2-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e1e2-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e1e2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1e2-130">CommonParameters</span></span>
<span data-ttu-id="0e1e2-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1e2-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e1e2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1e2-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e1e2-133">INPUTS</span></span>

### <span data-ttu-id="0e1e2-134">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0e1e2-134">VirtualMachineScaleSet</span></span>
<span data-ttu-id="0e1e2-135">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="0e1e2-135">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="0e1e2-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e1e2-136">OUTPUTS</span></span>

### <span data-ttu-id="0e1e2-137">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0e1e2-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0e1e2-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e1e2-138">NOTES</span></span>

## <span data-ttu-id="0e1e2-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e1e2-139">RELATED LINKS</span></span>

[<span data-ttu-id="0e1e2-140">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0e1e2-140">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


