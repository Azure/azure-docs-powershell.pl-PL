---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClientCertificate.md
ms.openlocfilehash: e508afc5ab66a3e2aec49131bf2c8bf0e9d31259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716823"
---
# <span data-ttu-id="3b5dc-101">Remove-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3b5dc-101">Remove-AzureRmServiceFabricClientCertificate</span></span>

## <span data-ttu-id="3b5dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b5dc-102">SYNOPSIS</span></span>
<span data-ttu-id="3b5dc-103">Usuwanie certyfikatów klienta lub nazw podmiotów certyfikatów z używania w celu uwierzytelnienia klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b5dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b5dc-104">SYNTAX</span></span>

### <span data-ttu-id="3b5dc-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="3b5dc-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b5dc-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="3b5dc-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b5dc-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="3b5dc-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b5dc-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="3b5dc-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzureRmServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b5dc-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3b5dc-109">DESCRIPTION</span></span>
<span data-ttu-id="3b5dc-110">Użyj narzędzia **Remove-AzureRmServiceFabricClientCertificate** w celu usunięcia certyfikatów klienta lub nazw podmiotów (s) certyfikatu z używania do uwierzytelniania klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-110">Use **Remove-AzureRmServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="3b5dc-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b5dc-111">EXAMPLES</span></span>

### <span data-ttu-id="3b5dc-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3b5dc-112">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="3b5dc-113">To polecenie usunie certyfikat klienta z odciskiem palca "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" z klastra.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="3b5dc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b5dc-114">PARAMETERS</span></span>

### <span data-ttu-id="3b5dc-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="3b5dc-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="3b5dc-116">Określ odcisk palca certyfikatu klienta, który ma tylko uprawnienia administratora.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-116">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5dc-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="3b5dc-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="3b5dc-118">Określanie nazwy pospolitej klienta, odcisku palca emitenta i typu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5dc-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="3b5dc-119">-CommonName</span></span>
<span data-ttu-id="3b5dc-120">Określ nazwę pospolitą certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-120">Specify client certificate common name.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5dc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b5dc-121">-DefaultProfile</span></span>
<span data-ttu-id="3b5dc-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b5dc-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="3b5dc-123">-IssuerThumbprint</span></span>
<span data-ttu-id="3b5dc-124">Określ odcisk palca wystawcy certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-124">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithCommonName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5dc-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b5dc-125">-Name</span></span>
<span data-ttu-id="3b5dc-126">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-126">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5dc-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="3b5dc-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="3b5dc-128">Określ odcisk palca certyfikatu klienta z uprawnieniem tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-128">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5dc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b5dc-129">-ResourceGroupName</span></span>
<span data-ttu-id="3b5dc-130">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-130">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5dc-131">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="3b5dc-131">-Thumbprint</span></span>
<span data-ttu-id="3b5dc-132">Określ odcisk palca certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-132">Specify client certificate thumbprint.</span></span>

```yaml
Type: String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b5dc-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b5dc-133">-Confirm</span></span>
<span data-ttu-id="3b5dc-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b5dc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b5dc-135">-WhatIf</span></span>
<span data-ttu-id="3b5dc-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3b5dc-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b5dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b5dc-138">CommonParameters</span></span>
<span data-ttu-id="3b5dc-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b5dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b5dc-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b5dc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b5dc-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b5dc-141">INPUTS</span></span>

### <span data-ttu-id="3b5dc-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3b5dc-142">System.Collections.Hashtable</span></span>
<span data-ttu-id="3b5dc-143">System. String</span><span class="sxs-lookup"><span data-stu-id="3b5dc-143">System.String</span></span>

<span data-ttu-id="3b5dc-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b5dc-144">System.Boolean</span></span>

## <span data-ttu-id="3b5dc-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b5dc-145">OUTPUTS</span></span>

### <span data-ttu-id="3b5dc-146">Microsoft. Azure. Commands. servicefabric. MODELES. PsCluster</span><span class="sxs-lookup"><span data-stu-id="3b5dc-146">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="3b5dc-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b5dc-147">NOTES</span></span>

## <span data-ttu-id="3b5dc-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b5dc-148">RELATED LINKS</span></span>

[<span data-ttu-id="3b5dc-149">Dodaj-AzureRmServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="3b5dc-149">Add-AzureRmServiceFabricClientCertificate</span></span>](./Add-AzureRmServiceFabricClientCertificate.md)
