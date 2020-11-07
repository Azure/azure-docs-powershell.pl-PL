---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 033f96abd50e6bc5260577b78e27904e5c361a98
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708084"
---
# <span data-ttu-id="13acb-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="13acb-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="13acb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13acb-102">SYNOPSIS</span></span>
<span data-ttu-id="13acb-103">Usuwanie certyfikatów klienta lub nazw podmiotów certyfikatów z używania w celu uwierzytelnienia klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="13acb-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="13acb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13acb-104">SYNTAX</span></span>

### <span data-ttu-id="13acb-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="13acb-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="13acb-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="13acb-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13acb-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="13acb-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13acb-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="13acb-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13acb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="13acb-109">DESCRIPTION</span></span>
<span data-ttu-id="13acb-110">Użyj narzędzia **Remove-AzServiceFabricClientCertificate** w celu usunięcia certyfikatów klienta lub nazw podmiotów (s) certyfikatu z używania do uwierzytelniania klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="13acb-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="13acb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13acb-111">EXAMPLES</span></span>

### <span data-ttu-id="13acb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="13acb-112">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="13acb-113">To polecenie usunie certyfikat klienta z odciskiem palca "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" z klastra.</span><span class="sxs-lookup"><span data-stu-id="13acb-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="13acb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13acb-114">PARAMETERS</span></span>

### <span data-ttu-id="13acb-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="13acb-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="13acb-116">Określ odcisk palca certyfikatu klienta, który ma tylko uprawnienia administratora.</span><span class="sxs-lookup"><span data-stu-id="13acb-116">Specify client certificate thumbprint that only has admin permission.</span></span>

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

### <span data-ttu-id="13acb-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="13acb-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="13acb-118">Określanie nazwy pospolitej klienta, odcisku palca emitenta i typu uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="13acb-118">Specify client common name, issuer thumbprint, and authentication type.</span></span>

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

### <span data-ttu-id="13acb-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="13acb-119">-CommonName</span></span>
<span data-ttu-id="13acb-120">Określ nazwę pospolitą certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="13acb-120">Specify client certificate common name.</span></span>

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

### <span data-ttu-id="13acb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13acb-121">-DefaultProfile</span></span>
<span data-ttu-id="13acb-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="13acb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13acb-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="13acb-123">-IssuerThumbprint</span></span>
<span data-ttu-id="13acb-124">Określ odcisk palca wystawcy certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="13acb-124">Specify client certificate issuer thumbprint.</span></span>

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

### <span data-ttu-id="13acb-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="13acb-125">-Name</span></span>
<span data-ttu-id="13acb-126">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="13acb-126">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="13acb-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="13acb-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="13acb-128">Określ odcisk palca certyfikatu klienta z uprawnieniem tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="13acb-128">Specify client certificate thumbprint that has read only permission.</span></span>

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

### <span data-ttu-id="13acb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13acb-129">-ResourceGroupName</span></span>
<span data-ttu-id="13acb-130">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="13acb-130">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="13acb-131">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="13acb-131">-Thumbprint</span></span>
<span data-ttu-id="13acb-132">Określ odcisk palca certyfikatu klienta.</span><span class="sxs-lookup"><span data-stu-id="13acb-132">Specify client certificate thumbprint.</span></span>

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

### <span data-ttu-id="13acb-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13acb-133">-Confirm</span></span>
<span data-ttu-id="13acb-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13acb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13acb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13acb-135">-WhatIf</span></span>
<span data-ttu-id="13acb-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13acb-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13acb-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13acb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13acb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13acb-138">CommonParameters</span></span>
<span data-ttu-id="13acb-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13acb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13acb-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13acb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13acb-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13acb-141">INPUTS</span></span>

### <span data-ttu-id="13acb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="13acb-142">System.String</span></span>

### <span data-ttu-id="13acb-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="13acb-143">System.String[]</span></span>

### <span data-ttu-id="13acb-144">Microsoft. Azure. Commands. servicefabric. MODELES. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="13acb-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="13acb-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13acb-145">OUTPUTS</span></span>

### <span data-ttu-id="13acb-146">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="13acb-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="13acb-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13acb-147">NOTES</span></span>

## <span data-ttu-id="13acb-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13acb-148">RELATED LINKS</span></span>

[<span data-ttu-id="13acb-149">Dodaj-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="13acb-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)