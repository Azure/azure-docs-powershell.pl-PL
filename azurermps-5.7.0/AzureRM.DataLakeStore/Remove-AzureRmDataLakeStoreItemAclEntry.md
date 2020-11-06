---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 41c1324c3762d0b6e04c0c532976c62c0a16067e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525145"
---
# <span data-ttu-id="1207f-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1207f-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="1207f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1207f-102">SYNOPSIS</span></span>
<span data-ttu-id="1207f-103">Usuwa wpis z listy ACL pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1207f-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1207f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1207f-104">SYNTAX</span></span>

### <span data-ttu-id="1207f-105">RemoveByACLObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1207f-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1207f-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="1207f-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1207f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1207f-107">DESCRIPTION</span></span>
<span data-ttu-id="1207f-108">Polecenie cmdlet **Remove-AzureRmDataLakeStoreItemAclEntry** usuwa wpis (ACE) z listy kontroli dostępu (ACL) pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1207f-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1207f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1207f-109">EXAMPLES</span></span>

### <span data-ttu-id="1207f-110">Przykład 1. Usuń wpis użytkownika</span><span class="sxs-lookup"><span data-stu-id="1207f-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="1207f-111">To polecenie usuwa wpis ACE użytkownika dla Patti z konta ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="1207f-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

## <span data-ttu-id="1207f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1207f-112">PARAMETERS</span></span>

### <span data-ttu-id="1207f-113">— Konto</span><span class="sxs-lookup"><span data-stu-id="1207f-113">-Account</span></span>
<span data-ttu-id="1207f-114">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1207f-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1207f-115">-AceType</span><span class="sxs-lookup"><span data-stu-id="1207f-115">-AceType</span></span>
<span data-ttu-id="1207f-116">Określa typ wpisu ACE do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="1207f-116">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="1207f-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1207f-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1207f-118">Konta</span><span class="sxs-lookup"><span data-stu-id="1207f-118">User</span></span>
- <span data-ttu-id="1207f-119">Grupowanie</span><span class="sxs-lookup"><span data-stu-id="1207f-119">Group</span></span>
- <span data-ttu-id="1207f-120">Usuń</span><span class="sxs-lookup"><span data-stu-id="1207f-120">Mask</span></span>
- <span data-ttu-id="1207f-121">Pozostałe</span><span class="sxs-lookup"><span data-stu-id="1207f-121">Other</span></span>

```yaml
Type: AceType
Parameter Sets: RemoveSpecificACE
Aliases: 
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1207f-122">-ACL</span><span class="sxs-lookup"><span data-stu-id="1207f-122">-Acl</span></span>
<span data-ttu-id="1207f-123">Określa obiekt ACL zawierający wpisy, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="1207f-123">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1207f-124">-Wartość domyślna</span><span class="sxs-lookup"><span data-stu-id="1207f-124">-Default</span></span>
<span data-ttu-id="1207f-125">Wskazuje, że ta operacja powoduje usunięcie domyślnego wpisu ACE z określonej listy ACL.</span><span class="sxs-lookup"><span data-stu-id="1207f-125">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1207f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1207f-126">-DefaultProfile</span></span>
<span data-ttu-id="1207f-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1207f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1207f-128">-ID</span><span class="sxs-lookup"><span data-stu-id="1207f-128">-Id</span></span>
<span data-ttu-id="1207f-129">Określa identyfikator obiektu użytkownika katalogu AzureActive, grupę lub podmiot zabezpieczeń usługi, dla którego ma zostać usunięty wpis ACE.</span><span class="sxs-lookup"><span data-stu-id="1207f-129">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: Guid
Parameter Sets: RemoveSpecificACE
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1207f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1207f-130">-PassThru</span></span>
<span data-ttu-id="1207f-131">Wskazuje, że należy zwrócić odpowiedź logiczną wskazującą wynik operacji usuwania.</span><span class="sxs-lookup"><span data-stu-id="1207f-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1207f-132">-Path</span><span class="sxs-lookup"><span data-stu-id="1207f-132">-Path</span></span>
<span data-ttu-id="1207f-133">Określa ścieżkę do usługi Data Lake Store, z której ma zostać usunięty wpis ACE, począwszy od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="1207f-133">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1207f-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1207f-134">-Confirm</span></span>
<span data-ttu-id="1207f-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1207f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1207f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1207f-136">-WhatIf</span></span>
<span data-ttu-id="1207f-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1207f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1207f-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1207f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1207f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1207f-139">CommonParameters</span></span>
<span data-ttu-id="1207f-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1207f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1207f-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1207f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1207f-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1207f-142">INPUTS</span></span>

### <span data-ttu-id="1207f-143">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="1207f-143">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="1207f-144">Parametr "ACL" przyjmuje wartość typu "DataLakeStoreItemAce []" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="1207f-144">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="1207f-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1207f-145">OUTPUTS</span></span>

### <span data-ttu-id="1207f-146">logiczną</span><span class="sxs-lookup"><span data-stu-id="1207f-146">bool</span></span>
<span data-ttu-id="1207f-147">Jeśli PassThru jest określony, zwraca wartość Prawda po poprawnym wykonaniu.</span><span class="sxs-lookup"><span data-stu-id="1207f-147">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="1207f-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1207f-148">NOTES</span></span>

## <span data-ttu-id="1207f-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1207f-149">RELATED LINKS</span></span>

[<span data-ttu-id="1207f-150">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1207f-150">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


