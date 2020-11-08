---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: c7a88cad933781b00e720c273be467966991cebf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219818"
---
# <span data-ttu-id="12742-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="12742-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="12742-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12742-102">SYNOPSIS</span></span>
<span data-ttu-id="12742-103">Usuwanie certyfikatów klienta lub nazw podmiotów certyfikatów z używania w celu uwierzytelnienia klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="12742-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="12742-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12742-104">SYNTAX</span></span>

### <span data-ttu-id="12742-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="12742-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12742-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="12742-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12742-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="12742-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12742-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="12742-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12742-109">Opis</span><span class="sxs-lookup"><span data-stu-id="12742-109">DESCRIPTION</span></span>
<span data-ttu-id="12742-110">Użyj narzędzia **Remove-AzServiceFabricClientCertificate** w celu usunięcia certyfikatów klienta lub nazw podmiotów (s) certyfikatu z używania do uwierzytelniania klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="12742-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="12742-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12742-111">EXAMPLES</span></span>

### <span data-ttu-id="12742-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="12742-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="12742-113">To polecenie usunie certyfikat klienta z odciskiem palca "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" z klastra.</span><span class="sxs-lookup"><span data-stu-id="12742-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="12742-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12742-114">PARAMETERS</span></span>

### <span data-ttu-id="12742-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="12742-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="12742-116">Określ odcisk palca certyfikatu klienta, który ma tylko uprawnienia administratora</span><span class="sxs-lookup"><span data-stu-id="12742-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="12742-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="12742-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="12742-118">Określanie nazwy pospolitej klienta, odcisku palca emitenta i typu uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="12742-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="12742-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="12742-119">-CommonName</span></span>
<span data-ttu-id="12742-120">Określanie nazwy pospolitej certyfikatu klienta</span><span class="sxs-lookup"><span data-stu-id="12742-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="12742-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12742-121">-DefaultProfile</span></span>
<span data-ttu-id="12742-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12742-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12742-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="12742-123">-IssuerThumbprint</span></span>
<span data-ttu-id="12742-124">Określanie odcisku palca wystawcy certyfikatu klienta</span><span class="sxs-lookup"><span data-stu-id="12742-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="12742-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12742-125">-Name</span></span>
<span data-ttu-id="12742-126">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="12742-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="12742-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="12742-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="12742-128">Określanie odcisku palca certyfikatu klienta, który ma tylko uprawnienia tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="12742-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="12742-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12742-129">-ResourceGroupName</span></span>
<span data-ttu-id="12742-130">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12742-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="12742-131">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="12742-131">-Thumbprint</span></span>
<span data-ttu-id="12742-132">Określanie odcisku palca certyfikatu klienta</span><span class="sxs-lookup"><span data-stu-id="12742-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="12742-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12742-133">-Confirm</span></span>
<span data-ttu-id="12742-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12742-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12742-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12742-135">-WhatIf</span></span>
<span data-ttu-id="12742-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12742-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12742-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12742-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12742-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12742-138">CommonParameters</span></span>
<span data-ttu-id="12742-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12742-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12742-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12742-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12742-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12742-141">INPUTS</span></span>

### <span data-ttu-id="12742-142">System. String</span><span class="sxs-lookup"><span data-stu-id="12742-142">System.String</span></span>

### <span data-ttu-id="12742-143">System. String []</span><span class="sxs-lookup"><span data-stu-id="12742-143">System.String[]</span></span>

### <span data-ttu-id="12742-144">Microsoft. Azure. Commands. servicefabric. MODELES. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="12742-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="12742-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12742-145">OUTPUTS</span></span>

### <span data-ttu-id="12742-146">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="12742-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="12742-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12742-147">NOTES</span></span>

## <span data-ttu-id="12742-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12742-148">RELATED LINKS</span></span>

[<span data-ttu-id="12742-149">Dodaj-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="12742-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
