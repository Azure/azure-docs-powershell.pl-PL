---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: FAAF458C-1662-4130-9A16-0514B714D11D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServer.md
ms.openlocfilehash: 9eb0e0503d1a7a7b71cac8f9f71a7c2f18847bca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542800"
---
# <span data-ttu-id="577aa-101">Set-AzureRmSqlServer</span><span class="sxs-lookup"><span data-stu-id="577aa-101">Set-AzureRmSqlServer</span></span>

## <span data-ttu-id="577aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="577aa-102">SYNOPSIS</span></span>
<span data-ttu-id="577aa-103">Modyfikuje właściwości serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="577aa-103">Modifies properties of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="577aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="577aa-104">SYNTAX</span></span>

```
Set-AzureRmSqlServer [-ServerName] <String> [-SqlAdministratorPassword <SecureString>] [-Tags <Hashtable>]
 [-ServerVersion <String>] [-AssignIdentity] [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="577aa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="577aa-105">DESCRIPTION</span></span>
<span data-ttu-id="577aa-106">Polecenie cmdlet **Set-AzureRmSqlServer** modyfikuje właściwości serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="577aa-106">The **Set-AzureRmSqlServer** cmdlet modifies properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="577aa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="577aa-107">EXAMPLES</span></span>

### <span data-ttu-id="577aa-108">Przykład 1: Resetowanie hasła administratora</span><span class="sxs-lookup"><span data-stu-id="577aa-108">Example 1: Reset the administrator password</span></span>
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
```

<span data-ttu-id="577aa-109">To polecenie resetuje hasło administratora na serwerze AzureSQL o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="577aa-109">This command resets the administrator password on the AzureSQL Server named server01.</span></span>

## <span data-ttu-id="577aa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="577aa-110">PARAMETERS</span></span>

### <span data-ttu-id="577aa-111">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="577aa-111">-AssignIdentity</span></span>
<span data-ttu-id="577aa-112">Wygeneruj i przypisz tożsamość usługi Azure Active Directory dla tego serwera do użytku z usługami zarządzania kluczami, takimi jak Magazyn kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="577aa-112">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="577aa-113">-Force</span><span class="sxs-lookup"><span data-stu-id="577aa-113">-Force</span></span>
<span data-ttu-id="577aa-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="577aa-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="577aa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="577aa-115">-ResourceGroupName</span></span>
<span data-ttu-id="577aa-116">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="577aa-116">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="577aa-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="577aa-117">-ServerName</span></span>
<span data-ttu-id="577aa-118">Określa nazwę serwera, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="577aa-118">Specifies the name of the server that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="577aa-119">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="577aa-119">-ServerVersion</span></span>
<span data-ttu-id="577aa-120">Określa wersję, do której to polecenie cmdlet zmieni serwer.</span><span class="sxs-lookup"><span data-stu-id="577aa-120">Specifies the version to which this cmdlet changes the server.</span></span> <span data-ttu-id="577aa-121">Dopuszczalne wartości tego parametru to: 2,0 i 12,0.</span><span class="sxs-lookup"><span data-stu-id="577aa-121">The acceptable values for this parameter are: 2.0 and 12.0.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577aa-122">-SqlAdministratorPassword</span><span class="sxs-lookup"><span data-stu-id="577aa-122">-SqlAdministratorPassword</span></span>
<span data-ttu-id="577aa-123">Określa nowe hasło jako element **SecureString** dla administratora serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="577aa-123">Specifies a new password, as a **SecureString** , for the database server administrator.</span></span> <span data-ttu-id="577aa-124">Aby uzyskać element **SecureString** , użyj polecenia cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="577aa-124">To obtain a **SecureString** , use the Get-Credential cmdlet.</span></span> <span data-ttu-id="577aa-125">Aby uzyskać więcej informacji, wpisz tekst `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="577aa-125">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577aa-126">-Tagi</span><span class="sxs-lookup"><span data-stu-id="577aa-126">-Tags</span></span>
<span data-ttu-id="577aa-127">Określa słownik tagów, które to polecenie cmdlet kojarzy z serwerem.</span><span class="sxs-lookup"><span data-stu-id="577aa-127">Specifies a dictionary of tags that this cmdlet associates with the server.</span></span> <span data-ttu-id="577aa-128">Pary klucz-wartość w formie tabeli skrótów ustawione jako znaczniki na serwerze.</span><span class="sxs-lookup"><span data-stu-id="577aa-128">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="577aa-129">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="577aa-129">For example:</span></span>

<span data-ttu-id="577aa-130">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="577aa-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="577aa-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="577aa-131">-Confirm</span></span>
<span data-ttu-id="577aa-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="577aa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="577aa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="577aa-133">-WhatIf</span></span>
<span data-ttu-id="577aa-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="577aa-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="577aa-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="577aa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="577aa-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="577aa-136">-DefaultProfile</span></span>
<span data-ttu-id="577aa-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="577aa-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="577aa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="577aa-138">CommonParameters</span></span>
<span data-ttu-id="577aa-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="577aa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="577aa-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="577aa-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="577aa-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="577aa-141">INPUTS</span></span>

## <span data-ttu-id="577aa-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="577aa-142">OUTPUTS</span></span>

### <span data-ttu-id="577aa-143">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="577aa-143">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="577aa-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="577aa-144">NOTES</span></span>

## <span data-ttu-id="577aa-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="577aa-145">RELATED LINKS</span></span>

[<span data-ttu-id="577aa-146">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="577aa-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
