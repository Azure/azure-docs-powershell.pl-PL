---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 1ed5b95346ffde947366696f30e54cfddcdea4d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005530"
---
# <span data-ttu-id="04345-101">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="04345-101">Remove-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="04345-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04345-102">SYNOPSIS</span></span>
<span data-ttu-id="04345-103">Usuwanie certyfikatów klientów lub podmiotów certyfikatów z uwierzytelniania klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="04345-103">Remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="04345-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="04345-104">SYNTAX</span></span>

### <span data-ttu-id="04345-105">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="04345-105">SingleUpdateWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -CommonName <String>
 -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04345-106">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="04345-106">SingleUpdateWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04345-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="04345-107">MultipleUpdatesWithCommonName</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04345-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="04345-108">MultipleUpdatesWithThumbprint</span></span>
```
Remove-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04345-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="04345-109">DESCRIPTION</span></span>
<span data-ttu-id="04345-110">Użyj **metody Remove-AzServiceFabricClientCertificate,** aby usunąć certyfikaty klientów lub podmioty certyfikatów z użycia w celu uwierzytelniania klienta w klastrze.</span><span class="sxs-lookup"><span data-stu-id="04345-110">Use **Remove-AzServiceFabricClientCertificate** to remove a client certificate(s) or certificate subject(s) name(s) from being used for client authentication to the cluster.</span></span>

## <span data-ttu-id="04345-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="04345-111">EXAMPLES</span></span>

### <span data-ttu-id="04345-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="04345-112">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="04345-113">To polecenie spowoduje usunięcie certyfikatu klienta ze znakiem usbprint "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" z klastra.</span><span class="sxs-lookup"><span data-stu-id="04345-113">This command will remove client certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' from the cluster.</span></span>

## <span data-ttu-id="04345-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04345-114">PARAMETERS</span></span>

### <span data-ttu-id="04345-115">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="04345-115">-AdminClientThumbprint</span></span>
<span data-ttu-id="04345-116">Określanie etykiety usbprint certyfikatu klienta, która ma tylko uprawnienia administratora</span><span class="sxs-lookup"><span data-stu-id="04345-116">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="04345-117">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="04345-117">-ClientCertificateCommonName</span></span>
<span data-ttu-id="04345-118">Określ nazwę pospolitą klienta, thumbprint wystawcy i typ uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="04345-118">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="04345-119">-CommonName</span><span class="sxs-lookup"><span data-stu-id="04345-119">-CommonName</span></span>
<span data-ttu-id="04345-120">Określanie wspólnej nazwy certyfikatu klienta</span><span class="sxs-lookup"><span data-stu-id="04345-120">Specify client certificate common name</span></span>

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

### <span data-ttu-id="04345-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04345-121">-DefaultProfile</span></span>
<span data-ttu-id="04345-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="04345-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04345-123">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="04345-123">-IssuerThumbprint</span></span>
<span data-ttu-id="04345-124">Określanie odcisku palca wystawcy certyfikatu klienta</span><span class="sxs-lookup"><span data-stu-id="04345-124">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="04345-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="04345-125">-Name</span></span>
<span data-ttu-id="04345-126">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="04345-126">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="04345-127">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="04345-127">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="04345-128">Określanie odcisku palca certyfikatu klienta, który ma uprawnienie tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="04345-128">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="04345-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04345-129">-ResourceGroupName</span></span>
<span data-ttu-id="04345-130">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="04345-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="04345-131">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="04345-131">-Thumbprint</span></span>
<span data-ttu-id="04345-132">Określanie odcisku palca certyfikatu klienta</span><span class="sxs-lookup"><span data-stu-id="04345-132">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="04345-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04345-133">-Confirm</span></span>
<span data-ttu-id="04345-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="04345-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04345-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04345-135">-WhatIf</span></span>
<span data-ttu-id="04345-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04345-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04345-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="04345-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04345-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04345-138">CommonParameters</span></span>
<span data-ttu-id="04345-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04345-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04345-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04345-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04345-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04345-141">INPUTS</span></span>

### <span data-ttu-id="04345-142">System.String</span><span class="sxs-lookup"><span data-stu-id="04345-142">System.String</span></span>

### <span data-ttu-id="04345-143">System.String[]</span><span class="sxs-lookup"><span data-stu-id="04345-143">System.String[]</span></span>

### <span data-ttu-id="04345-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="04345-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="04345-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04345-145">OUTPUTS</span></span>

### <span data-ttu-id="04345-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="04345-146">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="04345-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="04345-147">NOTES</span></span>

## <span data-ttu-id="04345-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04345-148">RELATED LINKS</span></span>

[<span data-ttu-id="04345-149">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="04345-149">Add-AzServiceFabricClientCertificate</span></span>](./Add-AzServiceFabricClientCertificate.md)
