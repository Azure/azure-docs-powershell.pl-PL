---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 14e1dd0b897ce5f5c9557ed5aa72c3f63a6514f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718213"
---
# <span data-ttu-id="9bfe6-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9bfe6-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="9bfe6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bfe6-102">SYNOPSIS</span></span>
<span data-ttu-id="9bfe6-103">Usuwa wpis z listy ACL pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bfe6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bfe6-104">SYNTAX</span></span>

### <span data-ttu-id="9bfe6-105">Usuwanie wpisów ACL przy użyciu obiektu ACL (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9bfe6-105">Remove ACL Entries using ACL object (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bfe6-106">Usuwanie określonego wpisu ACE</span><span class="sxs-lookup"><span data-stu-id="9bfe6-106">Remove specific ACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bfe6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9bfe6-107">DESCRIPTION</span></span>
<span data-ttu-id="9bfe6-108">Polecenie cmdlet **Remove-AzureRmDataLakeStoreItemAclEntry** usuwa wpis (ACE) z listy kontroli dostępu (ACL) pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="9bfe6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bfe6-109">EXAMPLES</span></span>

### <span data-ttu-id="9bfe6-110">Przykład 1. Usuń wpis użytkownika</span><span class="sxs-lookup"><span data-stu-id="9bfe6-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="9bfe6-111">To polecenie usuwa wpis ACE użytkownika dla Patti z konta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="9bfe6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bfe6-112">PARAMETERS</span></span>

### <span data-ttu-id="9bfe6-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="9bfe6-113">-Account</span></span>
<span data-ttu-id="9bfe6-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9bfe6-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="9bfe6-115">-AceType</span></span>
<span data-ttu-id="9bfe6-116">Określa typ wpisu ACE do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="9bfe6-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9bfe6-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9bfe6-118">Konta</span><span class="sxs-lookup"><span data-stu-id="9bfe6-118">User</span></span>
- <span data-ttu-id="9bfe6-119">Grupowanie</span><span class="sxs-lookup"><span data-stu-id="9bfe6-119">Group</span></span>
- <span data-ttu-id="9bfe6-120">Usuń</span><span class="sxs-lookup"><span data-stu-id="9bfe6-120">Mask</span></span>
- <span data-ttu-id="9bfe6-121">Pozostałe</span><span class="sxs-lookup"><span data-stu-id="9bfe6-121">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: Remove specific ACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfe6-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="9bfe6-122">-Acl</span></span>
<span data-ttu-id="9bfe6-123">Określa obiekt ACL zawierający wpisy, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: Remove ACL Entries using ACL object
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfe6-124">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="9bfe6-124">-Default</span></span>
<span data-ttu-id="9bfe6-125">Wskazuje, że ta operacja powoduje usunięcie domyślnego wpisu ACE z określonej listy ACL.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfe6-126">-ID</span><span class="sxs-lookup"><span data-stu-id="9bfe6-126">-Id</span></span>
<span data-ttu-id="9bfe6-127">Określa identyfikator obiektu użytkownika katalogu AzureActive, grupę lub podmiot zabezpieczeń usługi, dla którego ma zostać usunięty wpis ACE.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-127">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: Remove specific ACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfe6-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9bfe6-128">-PassThru</span></span>
<span data-ttu-id="9bfe6-129">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-129">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfe6-130">-Path</span><span class="sxs-lookup"><span data-stu-id="9bfe6-130">-Path</span></span>
<span data-ttu-id="9bfe6-131">Określa ścieżkę do usługi Data Lake Store, z której ma zostać usunięty wpis ACE, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="9bfe6-131">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bfe6-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9bfe6-132">-Confirm</span></span>
<span data-ttu-id="9bfe6-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bfe6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bfe6-134">-WhatIf</span></span>
<span data-ttu-id="9bfe6-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bfe6-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bfe6-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bfe6-137">-DefaultProfile</span></span>
<span data-ttu-id="9bfe6-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bfe6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bfe6-139">CommonParameters</span></span>
<span data-ttu-id="9bfe6-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bfe6-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bfe6-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bfe6-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bfe6-142">INPUTS</span></span>

### <span data-ttu-id="9bfe6-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="9bfe6-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="9bfe6-144">Parametr "ACL" przyjmuje wartość typu "DataLakeStoreItemAce []" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="9bfe6-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="9bfe6-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bfe6-145">OUTPUTS</span></span>

### <span data-ttu-id="9bfe6-146">logiczną</span><span class="sxs-lookup"><span data-stu-id="9bfe6-146">bool</span></span>
<span data-ttu-id="9bfe6-147">Jeśli PassThru jest określony, zwraca wartość Prawda po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="9bfe6-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="9bfe6-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bfe6-148">NOTES</span></span>

## <span data-ttu-id="9bfe6-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bfe6-149">RELATED LINKS</span></span>

[<span data-ttu-id="9bfe6-150">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9bfe6-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


