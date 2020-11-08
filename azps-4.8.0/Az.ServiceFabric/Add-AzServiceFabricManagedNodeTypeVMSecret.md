---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 36ed679066d1850851ff0e90f39eb6f9ef8ffa1a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063209"
---
# <span data-ttu-id="79a26-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="79a26-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="79a26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79a26-102">SYNOPSIS</span></span>
<span data-ttu-id="79a26-103">Dodaj klucz tajny certyfikatu do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="79a26-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="79a26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79a26-104">SYNTAX</span></span>

### <span data-ttu-id="79a26-105">ByObj (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79a26-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a26-106">ByName</span><span class="sxs-lookup"><span data-stu-id="79a26-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79a26-107">Opis</span><span class="sxs-lookup"><span data-stu-id="79a26-107">DESCRIPTION</span></span>
<span data-ttu-id="79a26-108">Dodaj klucz tajny certyfikatu do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="79a26-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="79a26-109">Klucz tajny musi być przechowywany w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="79a26-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="79a26-110">Aby uzyskać więcej informacji dotyczących magazynu kluczy, zobacz co to jest magazyn kluczy platformy Azure?</span><span class="sxs-lookup"><span data-stu-id="79a26-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="79a26-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="79a26-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="79a26-112">Aby uzyskać więcej informacji na temat poleceń cmdlet, zobacz polecenia cmdlet magazynu kluczy platformy Azure ( https://msdn.microsoft.com/library/azure/dn868052.aspx) w bibliotece Microsoft Developer Network lub polecenia cmdlet Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="79a26-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="79a26-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79a26-113">EXAMPLES</span></span>

### <span data-ttu-id="79a26-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79a26-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="79a26-115">Ten rozdzielony średnik dodaje wpis tajny certyfikatu z określonego magazynu kluczy i identyfikatora tajnego.</span><span class="sxs-lookup"><span data-stu-id="79a26-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="79a26-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="79a26-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="79a26-117">Ten rozdzielony średnik dodaje wpis tajny certyfikatu z określonego magazynu kluczy i identyfikatora tajnego z potokiem.</span><span class="sxs-lookup"><span data-stu-id="79a26-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="79a26-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79a26-118">PARAMETERS</span></span>

### <span data-ttu-id="79a26-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79a26-119">-AsJob</span></span>
<span data-ttu-id="79a26-120">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="79a26-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="79a26-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="79a26-121">-CertificateStore</span></span>
<span data-ttu-id="79a26-122">Określa magazyn certyfikatów na maszynie wirtualnej, do której ma zostać dodany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="79a26-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="79a26-123">Określony magazyn certyfikatów jest niejawny na koncie usługi LocalMachine.</span><span class="sxs-lookup"><span data-stu-id="79a26-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a26-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="79a26-124">-CertificateUrl</span></span>
<span data-ttu-id="79a26-125">Jest to adres URL certyfikatu, który został przekazany do magazynu kluczy jako klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="79a26-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="79a26-126">Aby dodać klucz tajny do magazynu kluczy, zobacz \[ Dodawanie klucza lub klucza tajnego do magazynu kluczy \] ( https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) .</span><span class="sxs-lookup"><span data-stu-id="79a26-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="79a26-127">W tym przypadku certyfikat musi być zakodowany przy użyciu kodowania base64 następującego obiektu JSON, który jest kodowany w formacie UTF-8: \<br\> \<br\> { \<br\> "dane": " \<Base64-encoded-certificate\> ", \<br\> "typ_danych", \<br\> "hasło": " \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="79a26-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a26-128">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="79a26-128">-ClusterName</span></span>
<span data-ttu-id="79a26-129">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="79a26-129">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a26-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a26-130">-DefaultProfile</span></span>
<span data-ttu-id="79a26-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79a26-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a26-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="79a26-132">-InputObject</span></span>
<span data-ttu-id="79a26-133">Zasób typu węzła</span><span class="sxs-lookup"><span data-stu-id="79a26-133">Node Type resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79a26-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79a26-134">-Name</span></span>
<span data-ttu-id="79a26-135">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="79a26-135">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a26-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a26-136">-ResourceGroupName</span></span>
<span data-ttu-id="79a26-137">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="79a26-137">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a26-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="79a26-138">-SourceVaultId</span></span>
<span data-ttu-id="79a26-139">Identyfikator zasobu magazynu kluczy zawierający certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="79a26-139">Key Vault resource id containing the certificates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a26-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79a26-140">-Confirm</span></span>
<span data-ttu-id="79a26-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a26-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a26-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a26-142">-WhatIf</span></span>
<span data-ttu-id="79a26-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79a26-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a26-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79a26-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a26-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a26-145">CommonParameters</span></span>
<span data-ttu-id="79a26-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79a26-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a26-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79a26-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a26-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79a26-148">INPUTS</span></span>

### <span data-ttu-id="79a26-149">System. String</span><span class="sxs-lookup"><span data-stu-id="79a26-149">System.String</span></span>

## <span data-ttu-id="79a26-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79a26-150">OUTPUTS</span></span>

### <span data-ttu-id="79a26-151">Microsoft. Azure. Commands. servicefabric. MODELES. PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="79a26-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="79a26-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79a26-152">NOTES</span></span>

## <span data-ttu-id="79a26-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79a26-153">RELATED LINKS</span></span>
