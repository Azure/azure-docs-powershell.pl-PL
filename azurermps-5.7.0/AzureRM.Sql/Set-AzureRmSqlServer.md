---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: f7d6dab2629dc8247cb404d1de2dc58b21fc8a2d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551476"
---
# <span data-ttu-id="c9beb-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="c9beb-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="c9beb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9beb-102">SYNOPSIS</span></span>
<span data-ttu-id="c9beb-103">Modyfikuje właściwości serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="c9beb-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9beb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9beb-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9beb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c9beb-105">DESCRIPTION</span></span>
<span data-ttu-id="c9beb-106">Polecenie cmdlet **Set-AzureRmSqlServer** modyfikuje właściwości serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c9beb-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="c9beb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9beb-107">EXAMPLES</span></span>

### <span data-ttu-id="c9beb-108">Przykład 1: Resetowanie hasła administratora</span><span class="sxs-lookup"><span data-stu-id="c9beb-108">Example 1: Reset the administrator password</span></span>
```
PS C:\>$ServerPassword = "newpassword"
PS C:\> $SecureString = ConvertTo-SecureString $ServerPassword -AsPlainText -Force
PS C:\> Set-AzureRmSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SqlAdministratorPassword $secureString
ResourceGroupName        : ResourceGroup01
ServerName               : Server01
Location                 : Australia East
SqlAdministratorLogin    : adminLogin
SqlAdministratorPassword :
ServerVersion            : 12.0
Tags                     :
Identity                 :
FullyQualifiedDomainName : server01.database.windows.net
```

<span data-ttu-id="c9beb-109">To polecenie resetuje hasło administratora na serwerze AzureSQL o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="c9beb-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="c9beb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9beb-110">PARAMETERS</span></span>

### <span data-ttu-id="c9beb-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c9beb-111">-AssignIdentity</span></span>
<span data-ttu-id="c9beb-112">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c9beb-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9beb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9beb-113">-DefaultProfile</span></span>
<span data-ttu-id="c9beb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c9beb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9beb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c9beb-115">-Force</span></span>
<span data-ttu-id="c9beb-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c9beb-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9beb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9beb-117">-ResourceGroupName</span></span>
<span data-ttu-id="c9beb-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="c9beb-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9beb-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c9beb-119">-ServerName</span></span>
<span data-ttu-id="c9beb-120">Określa nazwę serwera, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9beb-120">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9beb-121">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="c9beb-121">-ServerVersion</span></span>
<span data-ttu-id="c9beb-122">Określa wersję, do której to polecenie cmdlet zmieni serwer.</span><span class="sxs-lookup"><span data-stu-id="c9beb-122">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="c9beb-123">Dopuszczalne wartości tego parametru to: 2,0 i 12,0.</span><span class="sxs-lookup"><span data-stu-id="c9beb-123">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9beb-124">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="c9beb-124">-SqlAdministratorPassword</span></span>
<span data-ttu-id="c9beb-125">Określa nowe hasło jako element **SecureString** dla administratora serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c9beb-125">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="c9beb-126">Aby uzyskać element **SecureString** , użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="c9beb-126">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="c9beb-127">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="c9beb-127">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9beb-128">-Tagi</span><span class="sxs-lookup"><span data-stu-id="c9beb-128">-Tags</span></span>
<span data-ttu-id="c9beb-129">Określa słownik tagów, które to polecenie cmdlet kojarzy z serwerem.</span><span class="sxs-lookup"><span data-stu-id="c9beb-129">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="c9beb-130">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="c9beb-130">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="c9beb-131">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="c9beb-131">For example:</span></span>

<span data-ttu-id="c9beb-132">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="c9beb-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9beb-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9beb-133">-Confirm</span></span>
<span data-ttu-id="c9beb-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9beb-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9beb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9beb-135">-WhatIf</span></span>
<span data-ttu-id="c9beb-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9beb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9beb-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9beb-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9beb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9beb-138">CommonParameters</span></span>
<span data-ttu-id="c9beb-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9beb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9beb-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9beb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9beb-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9beb-141">INPUTS</span></span>

### <span data-ttu-id="c9beb-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c9beb-142">None</span></span>
<span data-ttu-id="c9beb-143">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="c9beb-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9beb-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9beb-144">OUTPUTS</span></span>

### <span data-ttu-id="c9beb-145">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="c9beb-145">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="c9beb-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9beb-146">NOTES</span></span>

## <span data-ttu-id="c9beb-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9beb-147">RELATED LINKS</span></span>

[<span data-ttu-id="c9beb-148">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c9beb-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
