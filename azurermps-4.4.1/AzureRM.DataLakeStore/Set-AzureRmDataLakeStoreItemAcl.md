---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 94f81e8256af9282cdd5e09c1ab2822bf99c772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719033"
---
# <span data-ttu-id="6006d-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="6006d-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="6006d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6006d-102">SYNOPSIS</span></span>
<span data-ttu-id="6006d-103">Modyfikuje listę ACL plików lub folderów w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6006d-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6006d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6006d-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6006d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6006d-105">DESCRIPTION</span></span>
<span data-ttu-id="6006d-106">Polecenie cmdlet **Set-AzureRmDataLakeStoreItemAcl** modyfikuje listę kontroli dostępu (ACL) pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6006d-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6006d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6006d-107">EXAMPLES</span></span>

### <span data-ttu-id="6006d-108">Przykład 1. Ustawianie listy ACL dla pliku i folderu</span><span class="sxs-lookup"><span data-stu-id="6006d-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="6006d-109">Pierwsze polecenie pobiera listę ACL katalogu głównego konta usługi ContosoADL, a następnie zapisuje je w zmiennej $ACL.</span><span class="sxs-lookup"><span data-stu-id="6006d-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="6006d-110">Drugie polecenie ustawia listę ACL dla pliku Test.txt z tą $ACL.</span><span class="sxs-lookup"><span data-stu-id="6006d-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="6006d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6006d-111">PARAMETERS</span></span>

### <span data-ttu-id="6006d-112">— Konto</span><span class="sxs-lookup"><span data-stu-id="6006d-112">-Account</span></span>
<span data-ttu-id="6006d-113">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6006d-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6006d-114">-ACL</span><span class="sxs-lookup"><span data-stu-id="6006d-114">-Acl</span></span>
<span data-ttu-id="6006d-115">Określa listę ACL dla pliku lub folderu.</span><span class="sxs-lookup"><span data-stu-id="6006d-115">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6006d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6006d-116">-PassThru</span></span>
<span data-ttu-id="6006d-117">Wskazuje, że wynikowa lista ACL powinna być zwracana.</span><span class="sxs-lookup"><span data-stu-id="6006d-117">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="6006d-118">-Path</span><span class="sxs-lookup"><span data-stu-id="6006d-118">-Path</span></span>
<span data-ttu-id="6006d-119">Określa ścieżkę pliku lub folderu w usłudze Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="6006d-119">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6006d-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6006d-120">-Confirm</span></span>
<span data-ttu-id="6006d-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6006d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6006d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6006d-122">-WhatIf</span></span>
<span data-ttu-id="6006d-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6006d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6006d-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6006d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6006d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6006d-125">-DefaultProfile</span></span>
<span data-ttu-id="6006d-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6006d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6006d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6006d-127">CommonParameters</span></span>
<span data-ttu-id="6006d-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6006d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6006d-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6006d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6006d-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6006d-130">INPUTS</span></span>

### <span data-ttu-id="6006d-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="6006d-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="6006d-132">Parametr "ACL" przyjmuje wartość typu "DataLakeStoreItemAce []" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="6006d-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="6006d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6006d-133">OUTPUTS</span></span>

### <span data-ttu-id="6006d-134">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="6006d-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="6006d-135">Jeśli PassThru jest określony, zwróci wynikową listę wpisów listy ACL.</span><span class="sxs-lookup"><span data-stu-id="6006d-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="6006d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6006d-136">NOTES</span></span>

## <span data-ttu-id="6006d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6006d-137">RELATED LINKS</span></span>

