---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: 37db0181ea135a0cdb00cddc0a18780fe9fe2d7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718692"
---
# <span data-ttu-id="ef018-101">Add-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ef018-101">Add-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="ef018-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef018-102">SYNOPSIS</span></span>
<span data-ttu-id="ef018-103">Dodawanie nazwy pospolitej lub odcisku palca do klastra w celu uwierzytelnienia klienta.</span><span class="sxs-lookup"><span data-stu-id="ef018-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef018-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef018-104">SYNTAX</span></span>

### <span data-ttu-id="ef018-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="ef018-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef018-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="ef018-106">SingleUpdateWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef018-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="ef018-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef018-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="ef018-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef018-109">Opis</span><span class="sxs-lookup"><span data-stu-id="ef018-109">DESCRIPTION</span></span>
<span data-ttu-id="ef018-110">Użyj **dodatku Add-AzureRmServiceFabricClientCertificate** , aby dodać do klastra nazwę pospolitą lub odcisk palca wystawcy certyfikatu, aby klient mógł go używać do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="ef018-110">Use **Add-AzureRmServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="ef018-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef018-111">EXAMPLES</span></span>

### <span data-ttu-id="ef018-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef018-112">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -IsAdmin
```

<span data-ttu-id="ef018-113">To polecenie doda certyfikat z odciskiem palca "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" do klastra, więc klient może użyć tego certyfikatu jako administratora do komunikacji z klastrem.</span><span class="sxs-lookup"><span data-stu-id="ef018-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="ef018-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ef018-114">Example 2</span></span>
```
PS c:> Add-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="ef018-115">To polecenie doda certyfikat klienta tylko do odczytu o nazwie "Contoso.com", a odcisk palca wystawcy to "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" do klastra.</span><span class="sxs-lookup"><span data-stu-id="ef018-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="ef018-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef018-116">PARAMETERS</span></span>

### <span data-ttu-id="ef018-117">-Administrator</span><span class="sxs-lookup"><span data-stu-id="ef018-117">-Admin</span></span>
<span data-ttu-id="ef018-118">Typ uwierzytelniania klienta.</span><span class="sxs-lookup"><span data-stu-id="ef018-118">Client authentication type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef018-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="ef018-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="ef018-120">Określ odcisk palca certyfikatu klienta, który ma tylko uprawnienia administratora.</span><span class="sxs-lookup"><span data-stu-id="ef018-120">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef018-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="ef018-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="ef018-122">Określanie nazwy pospolitej klienta, odcisku palca emitenta i typu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="ef018-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef018-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="ef018-123">-CommonName</span></span>
<span data-ttu-id="ef018-124">Określ nazwę pospolitą certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="ef018-124">Specify client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef018-125">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="ef018-125">-IssuerThumbprint</span></span>
<span data-ttu-id="ef018-126">Określ odcisk palca wystawcy certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="ef018-126">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef018-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ef018-127">-Name</span></span>
<span data-ttu-id="ef018-128">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="ef018-128">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef018-129">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="ef018-129">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="ef018-130">Określ odcisk palca certyfikatu klienta z uprawnieniem tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="ef018-130">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef018-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef018-131">-ResourceGroupName</span></span>
<span data-ttu-id="ef018-132">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ef018-132">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ef018-133">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="ef018-133">-Thumbprint</span></span>
<span data-ttu-id="ef018-134">Określ odcisk palca certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="ef018-134">Specify client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef018-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef018-135">-Confirm</span></span>
<span data-ttu-id="ef018-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef018-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef018-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef018-137">-WhatIf</span></span>
<span data-ttu-id="ef018-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef018-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef018-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef018-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef018-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef018-140">-DefaultProfile</span></span>
<span data-ttu-id="ef018-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef018-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef018-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef018-142">CommonParameters</span></span>
<span data-ttu-id="ef018-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef018-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef018-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef018-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef018-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef018-145">INPUTS</span></span>

### <span data-ttu-id="ef018-146">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ef018-146">System.Collections.Hashtable</span></span>
<span data-ttu-id="ef018-147">System. String</span><span class="sxs-lookup"><span data-stu-id="ef018-147">System.String</span></span>

<span data-ttu-id="ef018-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef018-148">System.Boolean</span></span>

## <span data-ttu-id="ef018-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef018-149">OUTPUTS</span></span>

### <span data-ttu-id="ef018-150">Microsoft. Azure. Commands. servicefabric. MODELES. PsCluster</span><span class="sxs-lookup"><span data-stu-id="ef018-150">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="ef018-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef018-151">NOTES</span></span>

## <span data-ttu-id="ef018-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef018-152">RELATED LINKS</span></span>

[<span data-ttu-id="ef018-153">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ef018-153">Remove-AzureRmServiceFabricClientCertificate</span></span>](./Remove-AzureRmServiceFabricClientCertificate.md)
