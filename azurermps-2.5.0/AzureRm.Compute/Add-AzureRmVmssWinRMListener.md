---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 987BD670-20F3-4105-A5BE-03E712AB2B56
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsswinrmlistener
schema: 2.0.0
ms.openlocfilehash: dd9c13298adac34a53ed2f97bbc1e3edc95892df
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898086"
---
# <span data-ttu-id="5aea5-101">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="5aea5-101">Add-AzureRmVmssWinRMListener</span></span>

## <span data-ttu-id="5aea5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5aea5-102">SYNOPSIS</span></span>
<span data-ttu-id="5aea5-103">Dodaje odbiornik usługi WinRM do VMSS.</span><span class="sxs-lookup"><span data-stu-id="5aea5-103">Adds a WinRM listener to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5aea5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5aea5-104">SYNTAX</span></span>

```
Add-AzureRmVmssWinRMListener [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Protocol] <ProtocolTypes>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5aea5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5aea5-105">DESCRIPTION</span></span>
<span data-ttu-id="5aea5-106">Polecenie cmdlet **Add-AzureRmVmssWinRMListener** umożliwia dodanie odbiornika zdalnego zarządzania systemem Windows (WinRM) na zestawie skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="5aea5-106">The **Add-AzureRmVmssWinRMListener** cmdlet adds a Windows Remote Management (WinRM) listener on the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5aea5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5aea5-107">EXAMPLES</span></span>

### <span data-ttu-id="5aea5-108">Przykład 1: Dodawanie odbiornika usługi WinRM do VMSS</span><span class="sxs-lookup"><span data-stu-id="5aea5-108">Example 1: Add a WinRM listener to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssWinRMListener -VirtualMachineScaleSet $VMSS -Protocol Https -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

<span data-ttu-id="5aea5-109">W tym przykładzie dodano odbiornik usługi WinRM do VMSS.</span><span class="sxs-lookup"><span data-stu-id="5aea5-109">This example adds a WinRM listener to the VMSS.</span></span>

<span data-ttu-id="5aea5-110">W pierwszym poleceniu użyto polecenia cmdlet **New-AzureRmVmssConfig** w celu utworzenia VMSS obiektu konfiguracji i zapisu wyniku w zmiennej o nazwie $VMSS.</span><span class="sxs-lookup"><span data-stu-id="5aea5-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="5aea5-111">Drugie polecenie dodaje odbiornik protokołu HTTP o usłudze WinRM z certyfikatem pod określonym adresem URL do VMSS.</span><span class="sxs-lookup"><span data-stu-id="5aea5-111">The second command adds an HTTP protocol WinRM listener with the certificate at the specified URL to the VMSS.</span></span>

## <span data-ttu-id="5aea5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5aea5-112">PARAMETERS</span></span>

### <span data-ttu-id="5aea5-113">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="5aea5-113">-CertificateUrl</span></span>
<span data-ttu-id="5aea5-114">Określa łącze (jako adres URL) certyfikatu, z którym Zainicjowano obsługę administracyjną nowych maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="5aea5-114">Specifies a link, as a URL, of the certificate with which new virtual machines are provisioned.</span></span>

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

### <span data-ttu-id="5aea5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aea5-115">-DefaultProfile</span></span>
<span data-ttu-id="5aea5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5aea5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5aea5-117">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="5aea5-117">-Protocol</span></span>
<span data-ttu-id="5aea5-118">Określa protokół odbiornika usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="5aea5-118">Specifies the protocol of the WinRM listener.</span></span>
<span data-ttu-id="5aea5-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5aea5-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5aea5-120">URL</span><span class="sxs-lookup"><span data-stu-id="5aea5-120">Http</span></span>
- <span data-ttu-id="5aea5-121">Https</span><span class="sxs-lookup"><span data-stu-id="5aea5-121">Https</span></span>

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

### <span data-ttu-id="5aea5-122">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5aea5-122">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5aea5-123">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="5aea5-123">Specifies the VMSS object.</span></span>
<span data-ttu-id="5aea5-124">Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzureRmVmssConfig.</span><span class="sxs-lookup"><span data-stu-id="5aea5-124">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="5aea5-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5aea5-125">-Confirm</span></span>
<span data-ttu-id="5aea5-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5aea5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aea5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aea5-127">-WhatIf</span></span>
<span data-ttu-id="5aea5-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5aea5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5aea5-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5aea5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aea5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aea5-130">CommonParameters</span></span>
<span data-ttu-id="5aea5-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aea5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aea5-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aea5-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aea5-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5aea5-133">INPUTS</span></span>

### <span data-ttu-id="5aea5-134">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5aea5-134">VirtualMachineScaleSet</span></span>
<span data-ttu-id="5aea5-135">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="5aea5-135">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="5aea5-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5aea5-136">OUTPUTS</span></span>

### <span data-ttu-id="5aea5-137">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5aea5-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5aea5-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5aea5-138">NOTES</span></span>

## <span data-ttu-id="5aea5-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5aea5-139">RELATED LINKS</span></span>

[<span data-ttu-id="5aea5-140">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5aea5-140">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


