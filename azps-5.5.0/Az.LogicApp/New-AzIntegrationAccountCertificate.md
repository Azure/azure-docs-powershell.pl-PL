---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 651ce1141e9a925d5571f8b70d8eecedb4a1e66d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203722"
---
# <span data-ttu-id="ddb95-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb95-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="ddb95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddb95-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb95-103">Tworzy certyfikat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ddb95-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="ddb95-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ddb95-104">SYNTAX</span></span>

### <span data-ttu-id="ddb95-105">Klucz Prywatny</span><span class="sxs-lookup"><span data-stu-id="ddb95-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddb95-106">Klucz Publiczny</span><span class="sxs-lookup"><span data-stu-id="ddb95-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddb95-107">Oba</span><span class="sxs-lookup"><span data-stu-id="ddb95-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddb95-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ddb95-108">DESCRIPTION</span></span>
<span data-ttu-id="ddb95-109">Polecenie **cmdlet New-AzIntegrationAccountCertificate** tworzy certyfikat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ddb95-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="ddb95-110">To polecenie cmdlet zwraca obiekt reprezentujący certyfikat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ddb95-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="ddb95-111">Określ nazwę konta integracji, nazwę grupy zasobów, nazwę certyfikatu, nazwę klucza, wersję klucza i identyfikator magazynu klucza.</span><span class="sxs-lookup"><span data-stu-id="ddb95-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="ddb95-112">Wartości plików parametrów szablonu określone w wierszu polecenia mają pierwszeństwo przed wartościami parametrów szablonu w obiekcie parametru szablonu.</span><span class="sxs-lookup"><span data-stu-id="ddb95-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="ddb95-113">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="ddb95-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ddb95-114">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="ddb95-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ddb95-115">Aby wykryć nazwy parametrów dynamicznych, wpisz łącznik (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić przez dostępne parametry.</span><span class="sxs-lookup"><span data-stu-id="ddb95-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ddb95-116">Jeśli pominiesz wymagany parametr szablonu, polecenie cmdlet wyświetli monit o wartość.</span><span class="sxs-lookup"><span data-stu-id="ddb95-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ddb95-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ddb95-117">EXAMPLES</span></span>

### <span data-ttu-id="ddb95-118">Przykład 1. Tworzenie certyfikatu konta integracji</span><span class="sxs-lookup"><span data-stu-id="ddb95-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="ddb95-119">To polecenie tworzy certyfikat konta integracji w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="ddb95-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="ddb95-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddb95-120">PARAMETERS</span></span>

### <span data-ttu-id="ddb95-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ddb95-121">-CertificateName</span></span>
<span data-ttu-id="ddb95-122">Określa nazwę certyfikatu konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ddb95-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="ddb95-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb95-123">-DefaultProfile</span></span>
<span data-ttu-id="ddb95-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ddb95-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddb95-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ddb95-125">-KeyName</span></span>
<span data-ttu-id="ddb95-126">Określa nazwę klucza certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="ddb95-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb95-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ddb95-127">-KeyVaultId</span></span>
<span data-ttu-id="ddb95-128">Określa identyfikator magazynu klucza.</span><span class="sxs-lookup"><span data-stu-id="ddb95-128">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb95-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="ddb95-129">-KeyVersion</span></span>
<span data-ttu-id="ddb95-130">Określa wersję klucza certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="ddb95-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb95-131">— Metadane</span><span class="sxs-lookup"><span data-stu-id="ddb95-131">-Metadata</span></span>
<span data-ttu-id="ddb95-132">Określa obiekt metadanych dla certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="ddb95-132">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb95-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ddb95-133">-Name</span></span>
<span data-ttu-id="ddb95-134">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="ddb95-134">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb95-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ddb95-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="ddb95-136">Określa ścieżkę pliku certyfikatu publicznego (cer).</span><span class="sxs-lookup"><span data-stu-id="ddb95-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddb95-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb95-137">-ResourceGroupName</span></span>
<span data-ttu-id="ddb95-138">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ddb95-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ddb95-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ddb95-139">-Confirm</span></span>
<span data-ttu-id="ddb95-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ddb95-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb95-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddb95-141">-WhatIf</span></span>
<span data-ttu-id="ddb95-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddb95-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddb95-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ddb95-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddb95-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb95-144">CommonParameters</span></span>
<span data-ttu-id="ddb95-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddb95-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb95-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddb95-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb95-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddb95-147">INPUTS</span></span>

### <span data-ttu-id="ddb95-148">System.String</span><span class="sxs-lookup"><span data-stu-id="ddb95-148">System.String</span></span>

## <span data-ttu-id="ddb95-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddb95-149">OUTPUTS</span></span>

### <span data-ttu-id="ddb95-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb95-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="ddb95-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ddb95-151">NOTES</span></span>

## <span data-ttu-id="ddb95-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddb95-152">RELATED LINKS</span></span>

[<span data-ttu-id="ddb95-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb95-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="ddb95-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb95-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="ddb95-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ddb95-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


