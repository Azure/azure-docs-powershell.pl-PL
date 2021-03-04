---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricmanagednodetypevmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricManagedNodeTypeVMSecret.md
ms.openlocfilehash: 35d755bc117ccc4379be8d7344d8e7170594d555
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969793"
---
# <span data-ttu-id="a995f-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="a995f-101">Add-AzServiceFabricManagedNodeTypeVMSecret</span></span>

## <span data-ttu-id="a995f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a995f-102">SYNOPSIS</span></span>
<span data-ttu-id="a995f-103">Dodaj klucz tajny certyfikatu do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="a995f-103">Add certificate secret to the node type.</span></span>

## <span data-ttu-id="a995f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a995f-104">SYNTAX</span></span>

### <span data-ttu-id="a995f-105">ByObj (Domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a995f-105">ByObj (Default)</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-InputObject] <PSManagedNodeType> -SourceVaultId <String>
 -CertificateUrl <String> -CertificateStore <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a995f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a995f-106">ByName</span></span>
```
Add-AzServiceFabricManagedNodeTypeVMSecret [-ResourceGroupName] <String> [-ClusterName] <String>
 [-Name] <String> -SourceVaultId <String> -CertificateUrl <String> -CertificateStore <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a995f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a995f-107">DESCRIPTION</span></span>
<span data-ttu-id="a995f-108">Dodaj klucz tajny certyfikatu do typu węzła.</span><span class="sxs-lookup"><span data-stu-id="a995f-108">Add certificate secret to the node type.</span></span> <span data-ttu-id="a995f-109">Klucz tajny musi być przechowywany w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a995f-109">The secret must be stored in an Azure Key Vault.</span></span> <span data-ttu-id="a995f-110">Aby uzyskać więcej informacji dotyczących magazynu kluczy, zobacz Co to jest magazyn kluczy platformy Azure?</span><span class="sxs-lookup"><span data-stu-id="a995f-110">For more information relating to Key Vault, see What is Azure Key Vault?</span></span> <span data-ttu-id="a995f-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="a995f-111">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span> <span data-ttu-id="a995f-112">Aby uzyskać więcej informacji o poleceniach cmdlet, zobacz polecenia cmdlet magazynu kluczy platformy Azure (w bibliotece Microsoft Developer Network lub Set-AzKeyVaultSecret https://msdn.microsoft.com/library/azure/dn868052.aspx) cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a995f-112">For more information about the cmdlets, see Azure Key Vault Cmdlets (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the Set-AzKeyVaultSecret cmdlet.</span></span>

## <span data-ttu-id="a995f-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a995f-113">EXAMPLES</span></span>

### <span data-ttu-id="a995f-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a995f-114">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Add-AzServiceFabricManagedNodeTypeVMSecret -ResourceGroupName $rgName -ClusterName $clusterName -NodeTypeName $NodeTypeName -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="a995f-115">Ten przecinek dodaje klucz tajny certyfikatu z określonego identyfikatora klucza i klucza.</span><span class="sxs-lookup"><span data-stu-id="a995f-115">This commad adds a certificate secret from the keyvault and secret identifier specified.</span></span>

### <span data-ttu-id="a995f-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a995f-116">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
$nodeType = Get-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName -Name $NodeTypeName

$nodeType | Add-AzServiceFabricManagedNodeTypeVMSecret -SourceVaultId /subscriptions/XXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/testRG/providers/Microsoft.KeyVault/vaults/testkv -CertificateUrl https://testskv.vault.azure.net:443/secrets/TestCert/xxxxxxxxxxxxxxxxxxxxxxxx -CertificateStore My -Verbose
```

<span data-ttu-id="a995f-117">Ten przecinek dodaje klucz tajny certyfikatu z określonego identyfikatora klucza i tajnego, za pomocą funkcji pipingu.</span><span class="sxs-lookup"><span data-stu-id="a995f-117">This commad adds a certificate secret from the keyvault and secret identifier specified, with piping.</span></span>

## <span data-ttu-id="a995f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a995f-118">PARAMETERS</span></span>

### <span data-ttu-id="a995f-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a995f-119">-AsJob</span></span>
<span data-ttu-id="a995f-120">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="a995f-120">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a995f-121">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="a995f-121">-CertificateStore</span></span>
<span data-ttu-id="a995f-122">Określa magazyn certyfikatów na komputerze wirtualnym, do którego ma zostać dodany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="a995f-122">Specifies the certificate store on the Virtual Machine to which the certificate should be added.</span></span>
<span data-ttu-id="a995f-123">Określony magazyn certyfikatów niejawnie znajduje się na koncie localMachine.</span><span class="sxs-lookup"><span data-stu-id="a995f-123">The specified certificate store is implicitly in the LocalMachine account.</span></span>

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

### <span data-ttu-id="a995f-124">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="a995f-124">-CertificateUrl</span></span>
<span data-ttu-id="a995f-125">Jest to adres URL certyfikatu, który został przekazany do magazynu kluczy jako tajny.</span><span class="sxs-lookup"><span data-stu-id="a995f-125">This is the URL of a certificate that has been uploaded to Key Vault as a secret.</span></span>
<span data-ttu-id="a995f-126">Aby uzyskać informacje o dodaniu klucza tajnego do magazynu kluczy, zobacz Dodawanie klucza lub klucza tajnego \[ do magazynu kluczy \] https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add) (.</span><span class="sxs-lookup"><span data-stu-id="a995f-126">For adding a secret to the Key Vault, see \[Add a key or secret to the key vault\](https://docs.microsoft.com/azure/key-vault/key-vault-get-started/#add).</span></span>
<span data-ttu-id="a995f-127">W tym przypadku certyfikat musi być kodowaniem Base64 następującego obiektu JSON, które jest zakodowane w formacie UTF-8: \<br\> \<br\> { \<br\> "data":" \<Base64-encoded-certificate\> ", \<br\> "dataType":"pfx", \<br\> "password":" \<pfx-file-password\> " \<br\> }/</span><span class="sxs-lookup"><span data-stu-id="a995f-127">In this case, your certificate needs to be It is the Base64 encoding of the following JSON Object which is encoded in UTF-8: \<br\>\<br\> {\<br\>  "data":"\<Base64-encoded-certificate\>",\<br\>  "dataType":"pfx",\<br\>  "password":"\<pfx-file-password\>"\<br\>}/</span></span>

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

### <span data-ttu-id="a995f-128">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a995f-128">-ClusterName</span></span>
<span data-ttu-id="a995f-129">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="a995f-129">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a995f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a995f-130">-DefaultProfile</span></span>
<span data-ttu-id="a995f-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a995f-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a995f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a995f-132">-InputObject</span></span>
<span data-ttu-id="a995f-133">Zasób Typu węzła</span><span class="sxs-lookup"><span data-stu-id="a995f-133">Node Type resource</span></span>

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

### <span data-ttu-id="a995f-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a995f-134">-Name</span></span>
<span data-ttu-id="a995f-135">Określ nazwę typu węzła.</span><span class="sxs-lookup"><span data-stu-id="a995f-135">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="a995f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a995f-136">-ResourceGroupName</span></span>
<span data-ttu-id="a995f-137">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a995f-137">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="a995f-138">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="a995f-138">-SourceVaultId</span></span>
<span data-ttu-id="a995f-139">Identyfikator zasobu magazynu kluczy zawierający certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="a995f-139">Key Vault resource id containing the certificates.</span></span>

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

### <span data-ttu-id="a995f-140">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a995f-140">-Confirm</span></span>
<span data-ttu-id="a995f-141">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a995f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a995f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a995f-142">-WhatIf</span></span>
<span data-ttu-id="a995f-143">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a995f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a995f-144">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a995f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a995f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a995f-145">CommonParameters</span></span>
<span data-ttu-id="a995f-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a995f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a995f-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a995f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a995f-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a995f-148">INPUTS</span></span>

### <span data-ttu-id="a995f-149">System.String</span><span class="sxs-lookup"><span data-stu-id="a995f-149">System.String</span></span>

## <span data-ttu-id="a995f-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a995f-150">OUTPUTS</span></span>

### <span data-ttu-id="a995f-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="a995f-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedNodeType</span></span>

## <span data-ttu-id="a995f-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a995f-152">NOTES</span></span>

## <span data-ttu-id="a995f-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a995f-153">RELATED LINKS</span></span>
