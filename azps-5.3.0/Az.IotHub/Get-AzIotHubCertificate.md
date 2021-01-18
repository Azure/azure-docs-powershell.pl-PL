---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 8bc586ea9543c7545e7d24e3bc6d7bc36bb77d49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503505"
---
# <span data-ttu-id="bb005-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="bb005-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="bb005-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bb005-102">SYNOPSIS</span></span>
<span data-ttu-id="bb005-103">Wyświetla listę wszystkich certyfikatów lub określony certyfikat zawarty w centrum usługi Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="bb005-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="bb005-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bb005-104">SYNTAX</span></span>

### <span data-ttu-id="bb005-105">ResourceSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bb005-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb005-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bb005-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb005-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bb005-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb005-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bb005-108">DESCRIPTION</span></span>
<span data-ttu-id="bb005-109">Aby uzyskać szczegółowe wyjaśnienie dotyczące certyfikatów urzędu certyfikacji w centrum usługi Azure IoT, zobacz https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="bb005-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="bb005-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bb005-110">EXAMPLES</span></span>

### <span data-ttu-id="bb005-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb005-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="bb005-112">Lista wszystkich certyfikatów w MyIotHub</span><span class="sxs-lookup"><span data-stu-id="bb005-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="bb005-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bb005-113">Example 2</span></span>
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

<span data-ttu-id="bb005-114">Pokaż szczegóły dotyczące certyfikatu moje certyfikaty</span><span class="sxs-lookup"><span data-stu-id="bb005-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="bb005-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bb005-115">PARAMETERS</span></span>

### <span data-ttu-id="bb005-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="bb005-116">-CertificateName</span></span>
<span data-ttu-id="bb005-117">Nazwa certyfikatu</span><span class="sxs-lookup"><span data-stu-id="bb005-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="bb005-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb005-118">-DefaultProfile</span></span>
<span data-ttu-id="bb005-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb005-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb005-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bb005-120">-InputObject</span></span>
<span data-ttu-id="bb005-121">Obiekt IotHub</span><span class="sxs-lookup"><span data-stu-id="bb005-121">IotHub Object</span></span>

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

### <span data-ttu-id="bb005-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bb005-122">-Name</span></span>
<span data-ttu-id="bb005-123">Nazwa Centrum IoT</span><span class="sxs-lookup"><span data-stu-id="bb005-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bb005-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb005-124">-ResourceGroupName</span></span>
<span data-ttu-id="bb005-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bb005-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bb005-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb005-126">-ResourceId</span></span>
<span data-ttu-id="bb005-127">Identyfikator zasobu IotHub</span><span class="sxs-lookup"><span data-stu-id="bb005-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bb005-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb005-128">CommonParameters</span></span>
<span data-ttu-id="bb005-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb005-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb005-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb005-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb005-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb005-131">INPUTS</span></span>

### <span data-ttu-id="bb005-132">Microsoft. Azure. Commands. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bb005-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bb005-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bb005-133">System.String</span></span>

## <span data-ttu-id="bb005-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bb005-134">OUTPUTS</span></span>

### <span data-ttu-id="bb005-135">Microsoft. Azure. Commands. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="bb005-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="bb005-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bb005-136">NOTES</span></span>

## <span data-ttu-id="bb005-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb005-137">RELATED LINKS</span></span>
