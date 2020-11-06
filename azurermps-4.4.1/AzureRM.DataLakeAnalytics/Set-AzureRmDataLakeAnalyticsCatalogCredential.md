---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: e82559ec366809613ba66af4c27a3b944869f074
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551064"
---
# <span data-ttu-id="6d0f7-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="6d0f7-101">Set-AzureRmDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="6d0f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6d0f7-102">SYNOPSIS</span></span>
<span data-ttu-id="6d0f7-103">Modyfikuje hasło poświadczeń wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d0f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6d0f7-104">SYNTAX</span></span>

### <span data-ttu-id="6d0f7-105">Określanie nazwy hosta i portu (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6d0f7-105">Specify host name and port (Default)</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d0f7-106">Określ pełny identyfikator URI</span><span class="sxs-lookup"><span data-stu-id="6d0f7-106">Specify full URI</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d0f7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6d0f7-107">DESCRIPTION</span></span>
<span data-ttu-id="6d0f7-108">Polecenie cmdlet Set-AzureRmDataLakeAnalyticsCatalogCredential modyfikuje hasło poświadczenia skojarzone z wykazem usługi Azure Data Lake Analytics Catalog.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-108">The Set-AzureRmDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="6d0f7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6d0f7-109">EXAMPLES</span></span>

### <span data-ttu-id="6d0f7-110">Przykład 1: modyfikowanie hasła poświadczenia skojarzonego z kontem</span><span class="sxs-lookup"><span data-stu-id="6d0f7-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="6d0f7-111">To polecenie ustawia hasło poświadczenia na hasło określone w polu NoweHasło.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="6d0f7-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6d0f7-112">PARAMETERS</span></span>

### <span data-ttu-id="6d0f7-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="6d0f7-113">-Account</span></span>
<span data-ttu-id="6d0f7-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="6d0f7-115">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="6d0f7-115">-Credential</span></span>
<span data-ttu-id="6d0f7-116">Określa nazwę i bieżące hasło poświadczenia do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="6d0f7-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="6d0f7-117">-CredentialName</span></span>
<span data-ttu-id="6d0f7-118">Określa nazwę poświadczenia do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="6d0f7-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="6d0f7-119">-DatabaseHost</span></span>
<span data-ttu-id="6d0f7-120">Określa nazwę hosta zewnętrznego źródła danych, z którym poświadczenie może nawiązać połączenie w formacie mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0f7-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6d0f7-121">-DatabaseName</span></span>
<span data-ttu-id="6d0f7-122">Określa nazwę bazy danych na koncie usługi Data Lake Analytics zawierającego poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="6d0f7-123">-NoweHasło</span><span class="sxs-lookup"><span data-stu-id="6d0f7-123">-NewPassword</span></span>
<span data-ttu-id="6d0f7-124">Określa nowe hasło dla poświadczenia</span><span class="sxs-lookup"><span data-stu-id="6d0f7-124">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="6d0f7-125">-Port</span><span class="sxs-lookup"><span data-stu-id="6d0f7-125">-Port</span></span>
<span data-ttu-id="6d0f7-126">Określa numer portu używany do nawiązywania połączenia z określonym DatabaseHost przy użyciu tego poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-126">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0f7-127">-URI</span><span class="sxs-lookup"><span data-stu-id="6d0f7-127">-Uri</span></span>
<span data-ttu-id="6d0f7-128">Określa pełny identyfikator URI (Uniform Resource Identifier) zewnętrznego źródła danych, z którym poświadczenie może nawiązać połączenie.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-128">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d0f7-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d0f7-129">-Confirm</span></span>
<span data-ttu-id="6d0f7-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d0f7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d0f7-131">-WhatIf</span></span>
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

### <span data-ttu-id="6d0f7-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d0f7-132">-DefaultProfile</span></span>
<span data-ttu-id="6d0f7-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d0f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d0f7-134">CommonParameters</span></span>
<span data-ttu-id="6d0f7-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d0f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d0f7-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d0f7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d0f7-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d0f7-137">INPUTS</span></span>

## <span data-ttu-id="6d0f7-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6d0f7-138">OUTPUTS</span></span>

### <span data-ttu-id="6d0f7-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6d0f7-139">None</span></span>

## <span data-ttu-id="6d0f7-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6d0f7-140">NOTES</span></span>

## <span data-ttu-id="6d0f7-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d0f7-141">RELATED LINKS</span></span>

