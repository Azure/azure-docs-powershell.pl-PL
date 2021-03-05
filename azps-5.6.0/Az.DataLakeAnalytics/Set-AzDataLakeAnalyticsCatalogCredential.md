---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 75E4E0FB-35A8-47DA-B606-45E073D04625
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogCredential.md
ms.openlocfilehash: 51af3aeffe5cf75835507e78b4638270b255fb29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988247"
---
# <span data-ttu-id="97017-101">Set-AzDataLakeAnalyticsCatalogCredential</span><span class="sxs-lookup"><span data-stu-id="97017-101">Set-AzDataLakeAnalyticsCatalogCredential</span></span>

## <span data-ttu-id="97017-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97017-102">SYNOPSIS</span></span>
<span data-ttu-id="97017-103">Modyfikuje hasło poświadczeń wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="97017-103">Modifies an Azure Data Lake Analytics catalog credential password.</span></span>

## <span data-ttu-id="97017-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="97017-104">SYNTAX</span></span>

### <span data-ttu-id="97017-105">SetByHostNameAndPort (domyślne)</span><span class="sxs-lookup"><span data-stu-id="97017-105">SetByHostNameAndPort (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-Uri] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97017-106">SetByFullURI</span><span class="sxs-lookup"><span data-stu-id="97017-106">SetByFullURI</span></span>
```
Set-AzDataLakeAnalyticsCatalogCredential [-Account] <String> [-DatabaseName] <String>
 [-CredentialName] <String> [-Credential] <PSCredential> [-NewPassword] <PSCredential> [-DatabaseHost] <String>
 [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97017-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="97017-107">DESCRIPTION</span></span>
<span data-ttu-id="97017-108">Polecenie Set-AzDataLakeAnalyticsCatalogCredential modyfikuje hasło poświadczeń skojarzone z wykazem usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="97017-108">The Set-AzDataLakeAnalyticsCatalogCredential cmdlet modifies a credential password associated with an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="97017-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="97017-109">EXAMPLES</span></span>

### <span data-ttu-id="97017-110">Przykład 1. Modyfikowanie hasła poświadczenia skojarzonego z kontem</span><span class="sxs-lookup"><span data-stu-id="97017-110">Example 1: Modify a credential's password associated with an account</span></span>
```
PS C:\> Set-AzDataLakeAnalyticsCatalogCredential -AccountName "ContosoAdlAccount" `
                  -DatabaseName "databaseName" `
                  -CredentialName "credName" `
                  -Credential (Get-Credential) `
                  -NewPassword (Get-Credential) `
                  -Host "example.contoso.com" -Port 8080
```

<span data-ttu-id="97017-111">To polecenie ustawia hasło poświadczeń na hasło określone w adresie NewPassword.</span><span class="sxs-lookup"><span data-stu-id="97017-111">This command sets the credential password to the password specified in NewPassword.</span></span>

## <span data-ttu-id="97017-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97017-112">PARAMETERS</span></span>

### <span data-ttu-id="97017-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="97017-113">-Account</span></span>
<span data-ttu-id="97017-114">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="97017-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="97017-115">- Credential</span><span class="sxs-lookup"><span data-stu-id="97017-115">-Credential</span></span>
<span data-ttu-id="97017-116">Określa nazwę i bieżące hasło poświadczenia do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="97017-116">Specifies the name and current password of the credential to modify.</span></span>

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

### <span data-ttu-id="97017-117">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="97017-117">-CredentialName</span></span>
<span data-ttu-id="97017-118">Określa nazwę poświadczenia do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="97017-118">Specifies the name of the credential to modify</span></span>

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

### <span data-ttu-id="97017-119">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="97017-119">-DatabaseHost</span></span>
<span data-ttu-id="97017-120">Określa nazwę hosta zewnętrznego źródła danych, z które mogą być nawiązywane poświadczenia, w formacie, z mydatabase.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="97017-120">Specifies the host name of the external data source the credential can connect to in the format mydatabase.contoso.com.</span></span>

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

### <span data-ttu-id="97017-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="97017-121">-DatabaseName</span></span>
<span data-ttu-id="97017-122">Określa nazwę bazy danych na koncie Data Lake Analytics trzymającym poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="97017-122">Specifies the name of the database in the Data Lake Analytics account holding the credential.</span></span>

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

### <span data-ttu-id="97017-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97017-123">-DefaultProfile</span></span>
<span data-ttu-id="97017-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="97017-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97017-125">-NewPassword</span><span class="sxs-lookup"><span data-stu-id="97017-125">-NewPassword</span></span>
<span data-ttu-id="97017-126">Określa nowe hasło dla poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="97017-126">Specifies the new password for the credential</span></span>

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

### <span data-ttu-id="97017-127">— Port</span><span class="sxs-lookup"><span data-stu-id="97017-127">-Port</span></span>
<span data-ttu-id="97017-128">Określa numer portu używanego do łączenia się z określonym hostem DatabaseHost przy użyciu tego poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="97017-128">Specifies the port number used to connect to the specified DatabaseHost using this credential.</span></span>

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

### <span data-ttu-id="97017-129">-Uri</span><span class="sxs-lookup"><span data-stu-id="97017-129">-Uri</span></span>
<span data-ttu-id="97017-130">Określa pełny identyfikator URI zewnętrznego źródła danych, z który może nawiązać połączenie to poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="97017-130">Specifies the full Uniform Resource Identifier (URI) of the external data source this credential can connect to.</span></span>

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

### <span data-ttu-id="97017-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97017-131">-Confirm</span></span>
<span data-ttu-id="97017-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="97017-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97017-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97017-133">-WhatIf</span></span>
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

### <span data-ttu-id="97017-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97017-134">CommonParameters</span></span>
<span data-ttu-id="97017-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97017-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97017-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97017-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97017-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97017-137">INPUTS</span></span>

### <span data-ttu-id="97017-138">System.String</span><span class="sxs-lookup"><span data-stu-id="97017-138">System.String</span></span>

### <span data-ttu-id="97017-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="97017-139">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="97017-140">System.Uri</span><span class="sxs-lookup"><span data-stu-id="97017-140">System.Uri</span></span>

### <span data-ttu-id="97017-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="97017-141">System.Int32</span></span>

## <span data-ttu-id="97017-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97017-142">OUTPUTS</span></span>

### <span data-ttu-id="97017-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span><span class="sxs-lookup"><span data-stu-id="97017-143">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlCredential</span></span>

## <span data-ttu-id="97017-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="97017-144">NOTES</span></span>

## <span data-ttu-id="97017-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97017-145">RELATED LINKS</span></span>
