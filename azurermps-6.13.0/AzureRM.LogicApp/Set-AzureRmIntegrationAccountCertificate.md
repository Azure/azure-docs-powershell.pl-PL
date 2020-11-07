---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 00acd3e13484fe2981d172b4331ff7848c78fc9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551223"
---
# <span data-ttu-id="bd048-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bd048-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="bd048-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd048-102">SYNOPSIS</span></span>
<span data-ttu-id="bd048-103">Modyfikuje certyfikat konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="bd048-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd048-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd048-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd048-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bd048-105">DESCRIPTION</span></span>
<span data-ttu-id="bd048-106">Polecenie cmdlet **Set-AzureRmIntegrationAccountCertificate** modyfikuje certyfikat konta integracji.</span><span class="sxs-lookup"><span data-stu-id="bd048-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="bd048-107">To polecenie cmdlet zwraca obiekt reprezentujący certyfikat konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="bd048-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="bd048-108">Określanie nazwy konta integracji, nazwy grupy zasobów i nazwy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bd048-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="bd048-109">Ten moduł obsługuje parametry dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="bd048-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bd048-110">Aby użyć parametru dynamicznego, wpisz go w poleceniu.</span><span class="sxs-lookup"><span data-stu-id="bd048-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bd048-111">Aby wykryć nazwy parametrów dynamicznych, wpisz znak łącznika (-) po nazwie polecenia cmdlet, a następnie naciskaj klawisz Tab, aby przechodzić między dostępnymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="bd048-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bd048-112">W przypadku pominięcia wymaganego parametru szablonu polecenie cmdlet monituje o podanie wartości.</span><span class="sxs-lookup"><span data-stu-id="bd048-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bd048-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd048-113">EXAMPLES</span></span>

### <span data-ttu-id="bd048-114">Przykład 1. Modyfikowanie certyfikatu konta integracji</span><span class="sxs-lookup"><span data-stu-id="bd048-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="bd048-115">To polecenie modyfikuje certyfikat konta integracyjnego w określonej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd048-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="bd048-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd048-116">PARAMETERS</span></span>

### <span data-ttu-id="bd048-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="bd048-117">-CertificateName</span></span>
<span data-ttu-id="bd048-118">Określa nazwę certyfikatu konta integracyjnego.</span><span class="sxs-lookup"><span data-stu-id="bd048-118">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd048-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd048-119">-DefaultProfile</span></span>
<span data-ttu-id="bd048-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bd048-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd048-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bd048-121">-Force</span></span>
<span data-ttu-id="bd048-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bd048-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bd048-123">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="bd048-123">-KeyName</span></span>
<span data-ttu-id="bd048-124">Określa nazwę klucza certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="bd048-124">Specifies the name of a certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd048-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="bd048-125">-KeyVaultId</span></span>
<span data-ttu-id="bd048-126">Określa identyfikator magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="bd048-126">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd048-127">-Wersja-</span><span class="sxs-lookup"><span data-stu-id="bd048-127">-KeyVersion</span></span>
<span data-ttu-id="bd048-128">Określa wersję klucza certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="bd048-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd048-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="bd048-129">-Metadata</span></span>
<span data-ttu-id="bd048-130">Określa obiekt metadanych dla certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="bd048-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="bd048-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd048-131">-Name</span></span>
<span data-ttu-id="bd048-132">Określa nazwę konta integracji.</span><span class="sxs-lookup"><span data-stu-id="bd048-132">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd048-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="bd048-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="bd048-134">Określa ścieżkę pliku certyfikatu publicznego (CER).</span><span class="sxs-lookup"><span data-stu-id="bd048-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd048-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd048-135">-ResourceGroupName</span></span>
<span data-ttu-id="bd048-136">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd048-136">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd048-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd048-137">-Confirm</span></span>
<span data-ttu-id="bd048-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd048-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd048-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd048-139">-WhatIf</span></span>
<span data-ttu-id="bd048-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd048-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd048-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd048-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd048-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd048-142">CommonParameters</span></span>
<span data-ttu-id="bd048-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd048-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd048-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd048-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd048-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd048-145">INPUTS</span></span>

### <span data-ttu-id="bd048-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bd048-146">System.String</span></span>

## <span data-ttu-id="bd048-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd048-147">OUTPUTS</span></span>

### <span data-ttu-id="bd048-148">Microsoft. Azure. Management. Logic. MODELES. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bd048-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="bd048-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd048-149">NOTES</span></span>

## <span data-ttu-id="bd048-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd048-150">RELATED LINKS</span></span>

[<span data-ttu-id="bd048-151">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bd048-151">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="bd048-152">Nowe — AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bd048-152">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="bd048-153">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="bd048-153">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

