---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubCertificate.md
ms.openlocfilehash: cc9bc7ef4171ea59f79f6e4687dddea4bc1dbae1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544292"
---
# <span data-ttu-id="afd6a-101">Remove-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="afd6a-101">Remove-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="afd6a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="afd6a-102">SYNOPSIS</span></span>
<span data-ttu-id="afd6a-103">Usuwa certyfikat centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="afd6a-103">Deletes an Azure IoT Hub certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="afd6a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="afd6a-104">SYNTAX</span></span>

### <span data-ttu-id="afd6a-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="afd6a-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName] <String>
 [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afd6a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="afd6a-106">InputObjectSet</span></span>
```
Remove-AzureRmIotHubCertificate [-InputObject] <PSCertificateDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afd6a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="afd6a-107">ResourceIdSet</span></span>
```
Remove-AzureRmIotHubCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afd6a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="afd6a-108">DESCRIPTION</span></span>
<span data-ttu-id="afd6a-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="afd6a-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="afd6a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="afd6a-110">EXAMPLES</span></span>

### <span data-ttu-id="afd6a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="afd6a-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="
```

<span data-ttu-id="afd6a-112">Usuwa certyfikat moje</span><span class="sxs-lookup"><span data-stu-id="afd6a-112">Deletes MyCertificate</span></span>

## <span data-ttu-id="afd6a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="afd6a-113">PARAMETERS</span></span>

### <span data-ttu-id="afd6a-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="afd6a-114">-CertificateName</span></span>
<span data-ttu-id="afd6a-115">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="afd6a-115">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd6a-116">-DefaultProfile</span></span>
<span data-ttu-id="afd6a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="afd6a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afd6a-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="afd6a-118">-Etag</span></span>
<span data-ttu-id="afd6a-119">Element ETag certyfikatu</span><span class="sxs-lookup"><span data-stu-id="afd6a-119">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd6a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="afd6a-120">-InputObject</span></span>
<span data-ttu-id="afd6a-121">Obiekt Certificate</span><span class="sxs-lookup"><span data-stu-id="afd6a-121">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="afd6a-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="afd6a-122">-Name</span></span>
<span data-ttu-id="afd6a-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="afd6a-123">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd6a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afd6a-124">-PassThru</span></span>
<span data-ttu-id="afd6a-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="afd6a-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="afd6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afd6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="afd6a-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="afd6a-127">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd6a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="afd6a-128">-ResourceId</span></span>
<span data-ttu-id="afd6a-129">Identyfikator zasobu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="afd6a-129">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="afd6a-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="afd6a-130">-Confirm</span></span>
<span data-ttu-id="afd6a-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd6a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afd6a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd6a-132">-WhatIf</span></span>
<span data-ttu-id="afd6a-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd6a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afd6a-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="afd6a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afd6a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd6a-135">CommonParameters</span></span>
<span data-ttu-id="afd6a-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd6a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd6a-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd6a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd6a-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="afd6a-138">INPUTS</span></span>

### <span data-ttu-id="afd6a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="afd6a-139">System.String</span></span>

## <span data-ttu-id="afd6a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="afd6a-140">OUTPUTS</span></span>

### <span data-ttu-id="afd6a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="afd6a-141">System.Boolean</span></span>

## <span data-ttu-id="afd6a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="afd6a-142">NOTES</span></span>

## <span data-ttu-id="afd6a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="afd6a-143">RELATED LINKS</span></span>

