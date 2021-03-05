---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 06a6f2ea8ffbd0d90689a24d3fcec5ca8222f9ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988163"
---
# <span data-ttu-id="2ac3b-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="2ac3b-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="2ac3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac3b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac3b-103">Lista wszystkich certyfikatów lub określonego certyfikatu zawartego w centrum Azure IoT Hub.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="2ac3b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2ac3b-104">SYNTAX</span></span>

### <span data-ttu-id="2ac3b-105">Zestaw zasobów (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2ac3b-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac3b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ac3b-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac3b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2ac3b-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ac3b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="2ac3b-108">DESCRIPTION</span></span>
<span data-ttu-id="2ac3b-109">Aby uzyskać szczegółowe objaśnienie certyfikatów urzędu certyfikacji w centrum Azure IoT Hub, zobacz https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="2ac3b-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="2ac3b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2ac3b-110">EXAMPLES</span></span>

### <span data-ttu-id="2ac3b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2ac3b-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="2ac3b-112">Lista wszystkich certyfikatów w aplikacji MyIotHub</span><span class="sxs-lookup"><span data-stu-id="2ac3b-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="2ac3b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2ac3b-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="2ac3b-114">Pokaż szczegóły dotyczące programu MyCertificate</span><span class="sxs-lookup"><span data-stu-id="2ac3b-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="2ac3b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ac3b-115">PARAMETERS</span></span>

### <span data-ttu-id="2ac3b-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2ac3b-116">-CertificateName</span></span>
<span data-ttu-id="2ac3b-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="2ac3b-117">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac3b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac3b-118">-DefaultProfile</span></span>
<span data-ttu-id="2ac3b-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ac3b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac3b-120">-InputObject</span></span>
<span data-ttu-id="2ac3b-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="2ac3b-121">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac3b-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2ac3b-122">-Name</span></span>
<span data-ttu-id="2ac3b-123">Nazwa Centrum Iot</span><span class="sxs-lookup"><span data-stu-id="2ac3b-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac3b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac3b-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ac3b-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2ac3b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2ac3b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ac3b-126">-ResourceId</span></span>
<span data-ttu-id="2ac3b-127">Identyfikator zasobu w aplikacji IotHub</span><span class="sxs-lookup"><span data-stu-id="2ac3b-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2ac3b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac3b-128">CommonParameters</span></span>
<span data-ttu-id="2ac3b-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac3b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac3b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac3b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac3b-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ac3b-131">INPUTS</span></span>

### <span data-ttu-id="2ac3b-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2ac3b-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2ac3b-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2ac3b-133">System.String</span></span>

## <span data-ttu-id="2ac3b-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ac3b-134">OUTPUTS</span></span>

### <span data-ttu-id="2ac3b-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="2ac3b-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="2ac3b-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2ac3b-136">NOTES</span></span>

## <span data-ttu-id="2ac3b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ac3b-137">RELATED LINKS</span></span>
