---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: 913b610bc1d79c7a1792c06b53947fd3bf51151a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049839"
---
# <span data-ttu-id="779e2-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="779e2-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="779e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="779e2-102">SYNOPSIS</span></span>
<span data-ttu-id="779e2-103">Dodawanie nazwy pospolitej lub odcisku palca do klastra w celu uwierzytelnienia klienta.</span><span class="sxs-lookup"><span data-stu-id="779e2-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="779e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="779e2-104">SYNTAX</span></span>

### <span data-ttu-id="779e2-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="779e2-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="779e2-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="779e2-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="779e2-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="779e2-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="779e2-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="779e2-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="779e2-109">Opis</span><span class="sxs-lookup"><span data-stu-id="779e2-109">DESCRIPTION</span></span>
<span data-ttu-id="779e2-110">Użyj **dodatku Add-AzServiceFabricClientCertificate** , aby dodać do klastra nazwę pospolitą lub odcisk palca wystawcy certyfikatu, aby klient mógł go używać do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="779e2-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="779e2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="779e2-111">EXAMPLES</span></span>

### <span data-ttu-id="779e2-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="779e2-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="779e2-113">To polecenie doda certyfikat z odciskiem palca "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" do klastra, więc klient może użyć tego certyfikatu jako administratora do komunikacji z klastrem.</span><span class="sxs-lookup"><span data-stu-id="779e2-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="779e2-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="779e2-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="779e2-115">To polecenie doda certyfikat klienta tylko do odczytu o nazwie "Contoso.com", a odcisk palca wystawcy to "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" do klastra.</span><span class="sxs-lookup"><span data-stu-id="779e2-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="779e2-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="779e2-116">PARAMETERS</span></span>

### <span data-ttu-id="779e2-117">-Administrator</span><span class="sxs-lookup"><span data-stu-id="779e2-117">-Admin</span></span>
<span data-ttu-id="779e2-118">Typ uwierzytelniania klienta</span><span class="sxs-lookup"><span data-stu-id="779e2-118">Client authentication type</span></span>

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

### <span data-ttu-id="779e2-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="779e2-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="779e2-120">Określ odcisk palca certyfikatu klienta, który ma tylko uprawnienia administratora</span><span class="sxs-lookup"><span data-stu-id="779e2-120">Specify client certificate thumbprint which only has admin permission</span></span>

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

### <span data-ttu-id="779e2-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="779e2-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="779e2-122">Określanie nazwy pospolitej klienta, odcisku palca emitenta i typu uwierzytelniania</span><span class="sxs-lookup"><span data-stu-id="779e2-122">Specify client common name , issuer thumbprint and authentication type</span></span>

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

### <span data-ttu-id="779e2-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="779e2-123">-CommonName</span></span>
<span data-ttu-id="779e2-124">Określanie nazwy pospolitej certyfikatu klienta</span><span class="sxs-lookup"><span data-stu-id="779e2-124">Specify client certificate common name</span></span>

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

### <span data-ttu-id="779e2-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="779e2-125">-DefaultProfile</span></span>
<span data-ttu-id="779e2-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="779e2-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="779e2-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="779e2-127">-IssuerThumbprint</span></span>
<span data-ttu-id="779e2-128">Określanie odcisku palca wystawcy certyfikatu klienta</span><span class="sxs-lookup"><span data-stu-id="779e2-128">Specify thumbprint of client certificate's issuer</span></span>

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

### <span data-ttu-id="779e2-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="779e2-129">-Name</span></span>
<span data-ttu-id="779e2-130">Określanie nazwy klastra</span><span class="sxs-lookup"><span data-stu-id="779e2-130">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="779e2-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="779e2-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="779e2-132">Określanie odcisku palca certyfikatu klienta, który ma tylko uprawnienia tylko do odczytu</span><span class="sxs-lookup"><span data-stu-id="779e2-132">Specify client certificate thumbprint which only has read only permission</span></span>

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

### <span data-ttu-id="779e2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="779e2-133">-ResourceGroupName</span></span>
<span data-ttu-id="779e2-134">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="779e2-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="779e2-135">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="779e2-135">-Thumbprint</span></span>
<span data-ttu-id="779e2-136">Określanie odcisku palca certyfikatu klienta</span><span class="sxs-lookup"><span data-stu-id="779e2-136">Specify client certificate thumbprint</span></span>

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

### <span data-ttu-id="779e2-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="779e2-137">-Confirm</span></span>
<span data-ttu-id="779e2-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="779e2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="779e2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="779e2-139">-WhatIf</span></span>
<span data-ttu-id="779e2-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="779e2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="779e2-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="779e2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="779e2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="779e2-142">CommonParameters</span></span>
<span data-ttu-id="779e2-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="779e2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="779e2-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="779e2-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="779e2-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="779e2-145">INPUTS</span></span>

### <span data-ttu-id="779e2-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="779e2-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="779e2-147">System. String</span><span class="sxs-lookup"><span data-stu-id="779e2-147">System.String</span></span>

### <span data-ttu-id="779e2-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="779e2-148">System.String[]</span></span>

### <span data-ttu-id="779e2-149">Microsoft. Azure. Commands. servicefabric. MODELES. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="779e2-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="779e2-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="779e2-150">OUTPUTS</span></span>

### <span data-ttu-id="779e2-151">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="779e2-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="779e2-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="779e2-152">NOTES</span></span>

## <span data-ttu-id="779e2-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="779e2-153">RELATED LINKS</span></span>

[<span data-ttu-id="779e2-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="779e2-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
