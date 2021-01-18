---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 8d188e2f19c04792ea29cadef9d9ef71c20cfce9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503554"
---
# <span data-ttu-id="953ed-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="953ed-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="953ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="953ed-102">SYNOPSIS</span></span>
<span data-ttu-id="953ed-103">Modyfikuje hasło poświadczeń wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="953ed-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="953ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="953ed-104">SYNTAX</span></span>

### <span data-ttu-id="953ed-105">SetByHostNameAndPort (domyślny)</span><span class="sxs-lookup"><span data-stu-id="953ed-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="953ed-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="953ed-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="953ed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="953ed-107">DESCRIPTION</span></span>
<span data-ttu-id="953ed-108">Polecenie cmdlet Set-AzDataLakeAnalyticsCatalogCredential modyfikuje hasło poświadczenia skojarzone z wykazem usługi Azure Data Lake Analytics Catalog.</span><span class="sxs-lookup"><span data-stu-id="953ed-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="953ed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="953ed-109">EXAMPLES</span></span>

### <span data-ttu-id="953ed-110">Przykład 1: modyfikowanie hasła poświadczenia skojarzonego z kontem</span><span class="sxs-lookup"><span data-stu-id="953ed-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="953ed-111">To polecenie ustawia hasło poświadczenia na hasło określone w polu NoweHasło.</span><span class="sxs-lookup"><span data-stu-id="953ed-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="953ed-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="953ed-112">PARAMETERS</span></span>

### <span data-ttu-id="953ed-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="953ed-113">-Account</span></span>
<span data-ttu-id="953ed-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="953ed-114">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953ed-115">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="953ed-115">-Credential</span></span>
<span data-ttu-id="953ed-116">Określa nazwę i bieżące hasło poświadczenia do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="953ed-116">Specifies the name and current password of the credential to modify.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953ed-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="953ed-117">-CredentialName</span></span>
<span data-ttu-id="953ed-118">Określa nazwę poświadczenia do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="953ed-118">Specifies the name of the credential to modify</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953ed-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="953ed-119">-DatabaseHost</span></span>
<span data-ttu-id="953ed-120">Określa nazwę hosta zewnętrznego źródła danych, z którym poświadczenie może nawiązać połączenie w formacie mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="953ed-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953ed-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="953ed-121">-DatabaseName</span></span>
<span data-ttu-id="953ed-122">Określa nazwę bazy danych na koncie usługi Data Lake Analytics zawierającego poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="953ed-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953ed-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953ed-123">-DefaultProfile</span></span>
<span data-ttu-id="953ed-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="953ed-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="953ed-125">-NoweHasło</span><span class="sxs-lookup"><span data-stu-id="953ed-125">-NewPassword</span></span>
<span data-ttu-id="953ed-126">Określa nowe hasło dla poświadczenia</span><span class="sxs-lookup"><span data-stu-id="953ed-126">Specifies the new password for the credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953ed-127">-Port</span><span class="sxs-lookup"><span data-stu-id="953ed-127">-Port</span></span>
<span data-ttu-id="953ed-128">Określa numer portu używany do nawiązywania połączenia z określonym DatabaseHost przy użyciu tego poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="953ed-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetByFullURI
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953ed-129">-URI</span><span class="sxs-lookup"><span data-stu-id="953ed-129">-Uri</span></span>
<span data-ttu-id="953ed-130">Określa pełny identyfikator URI (Uniform Resource Identifier) zewnętrznego źródła danych, z którym poświadczenie może nawiązać połączenie.</span><span class="sxs-lookup"><span data-stu-id="953ed-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: SetByHostNameAndPort
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="953ed-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="953ed-131">-Confirm</span></span>
<span data-ttu-id="953ed-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="953ed-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="953ed-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="953ed-133">-WhatIf</span></span>
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

### <span data-ttu-id="953ed-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953ed-134">CommonParameters</span></span>
<span data-ttu-id="953ed-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="953ed-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953ed-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="953ed-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953ed-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="953ed-137">INPUTS</span></span>

### <span data-ttu-id="953ed-138">System. String</span><span class="sxs-lookup"><span data-stu-id="953ed-138">System.String</span></span>

### <span data-ttu-id="953ed-139">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="953ed-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="953ed-140">System. URI</span><span class="sxs-lookup"><span data-stu-id="953ed-140">System.Uri</span></span>

### <span data-ttu-id="953ed-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="953ed-141">System.Int32</span></span>

## <span data-ttu-id="953ed-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="953ed-142">OUTPUTS</span></span>

### <span data-ttu-id="953ed-143">Microsoft. Azure. Management. datalake. Analytics. modele. USqlCredential</span><span class="sxs-lookup"><span data-stu-id="953ed-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="953ed-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="953ed-144">NOTES</span></span>

## <span data-ttu-id="953ed-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="953ed-145">RELATED LINKS</span></span>
