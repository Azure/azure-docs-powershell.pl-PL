---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubCertificate.md
ms.openlocfilehash: 3e30b7aa3d1e43844fc1fe53e860ee8b8c66f385
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224302"
---
# <span data-ttu-id="56422-101">Remove-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="56422-101">Remove-AzIotHubCertificate</span></span>

## <span data-ttu-id="56422-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56422-102">SYNOPSIS</span></span>
<span data-ttu-id="56422-103">Usuwa certyfikat centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="56422-103">Deletes an Azure IoT Hub certificate.</span></span>

## <span data-ttu-id="56422-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56422-104">SYNTAX</span></span>

### <span data-ttu-id="56422-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="56422-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56422-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="56422-106">InputObjectSet</span></span>
```
Remove-AzIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56422-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="56422-107">ResourceIdSet</span></span>
```
Remove-AzIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56422-108">Opis</span><span class="sxs-lookup"><span data-stu-id="56422-108">DESCRIPTION</span></span>
<span data-ttu-id="56422-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="56422-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="56422-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56422-110">EXAMPLES</span></span>

### <span data-ttu-id="56422-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56422-111">Example 1</span></span>
```
PS C:\> Remove-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="56422-112">Usuwa certyfikat moje</span><span class="sxs-lookup"><span data-stu-id="56422-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="56422-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56422-113">PARAMETERS</span></span>

### <span data-ttu-id="56422-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="56422-114">-CertificateName</span></span>
<span data-ttu-id="56422-115">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="56422-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56422-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56422-116">-DefaultProfile</span></span>
<span data-ttu-id="56422-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56422-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56422-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="56422-118">-Etag</span></span>
<span data-ttu-id="56422-119">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="56422-119">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56422-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="56422-120">-InputObject</span></span>
<span data-ttu-id="56422-121">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="56422-121">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56422-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56422-122">-Name</span></span>
<span data-ttu-id="56422-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="56422-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56422-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56422-124">-PassThru</span></span>
<span data-ttu-id="56422-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="56422-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="56422-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56422-126">-ResourceGroupName</span></span>
<span data-ttu-id="56422-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="56422-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56422-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56422-128">-ResourceId</span></span>
<span data-ttu-id="56422-129">Identyfikator zasobu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="56422-129">Certificate Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56422-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="56422-130">-Confirm</span></span>
<span data-ttu-id="56422-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56422-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56422-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56422-132">-WhatIf</span></span>
<span data-ttu-id="56422-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56422-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56422-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="56422-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56422-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56422-135">CommonParameters</span></span>
<span data-ttu-id="56422-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56422-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56422-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56422-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56422-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56422-138">INPUTS</span></span>

### <span data-ttu-id="56422-139">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="56422-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="56422-140">System. String</span><span class="sxs-lookup"><span data-stu-id="56422-140">System.String</span></span>

## <span data-ttu-id="56422-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56422-141">OUTPUTS</span></span>

### <span data-ttu-id="56422-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56422-142">System.Boolean</span></span>

## <span data-ttu-id="56422-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56422-143">NOTES</span></span>

## <span data-ttu-id="56422-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56422-144">RELATED LINKS</span></span>
