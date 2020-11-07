---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: fc71ec338303876a2cff44a07632e9fae5d3d2d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719651"
---
# <span data-ttu-id="61b79-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="61b79-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="61b79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61b79-102">SYNOPSIS</span></span>
<span data-ttu-id="61b79-103">Modyfikuje właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="61b79-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61b79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61b79-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61b79-105">Opis</span><span class="sxs-lookup"><span data-stu-id="61b79-105">DESCRIPTION</span></span>
<span data-ttu-id="61b79-106">Polecenie cmdlet **Set-AzureRmDataLakeStoreItemOwner** modyfikuje właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="61b79-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="61b79-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61b79-107">EXAMPLES</span></span>

### <span data-ttu-id="61b79-108">Przykład 1. Ustawianie właściciela elementu</span><span class="sxs-lookup"><span data-stu-id="61b79-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="61b79-109">To polecenie ustawia właściciela katalogu głównego, aby Patti pełen.</span><span class="sxs-lookup"><span data-stu-id="61b79-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="61b79-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61b79-110">PARAMETERS</span></span>

### <span data-ttu-id="61b79-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="61b79-111">-Account</span></span>
<span data-ttu-id="61b79-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="61b79-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="61b79-113">-ID</span><span class="sxs-lookup"><span data-stu-id="61b79-113">-Id</span></span>
<span data-ttu-id="61b79-114">Określa identyfikator obiektu użytkownika, grupy lub podmiotu zabezpieczeń usługi AzureActive, który ma być używany jako właściciel.</span><span class="sxs-lookup"><span data-stu-id="61b79-114">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61b79-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61b79-115">-PassThru</span></span>
<span data-ttu-id="61b79-116">Wskazuje, że zaktualizowany właściciel powinien zostać zwrócony.</span><span class="sxs-lookup"><span data-stu-id="61b79-116">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="61b79-117">-Path</span><span class="sxs-lookup"><span data-stu-id="61b79-117">-Path</span></span>
<span data-ttu-id="61b79-118">Określa ścieżkę elementu, który należy zmodyfikować, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="61b79-118">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="61b79-119">-Type</span><span class="sxs-lookup"><span data-stu-id="61b79-119">-Type</span></span>
<span data-ttu-id="61b79-120">Określa typ właściciela do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="61b79-120">Specifies the type of owner to set.</span></span>
<span data-ttu-id="61b79-121">Dopuszczalne wartości tego parametru to: użytkownik i Grupa.</span><span class="sxs-lookup"><span data-stu-id="61b79-121">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases: 
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61b79-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61b79-122">-Confirm</span></span>
<span data-ttu-id="61b79-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61b79-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61b79-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61b79-124">-WhatIf</span></span>
<span data-ttu-id="61b79-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61b79-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61b79-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61b79-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61b79-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61b79-127">-DefaultProfile</span></span>
<span data-ttu-id="61b79-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61b79-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61b79-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61b79-129">CommonParameters</span></span>
<span data-ttu-id="61b79-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61b79-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61b79-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61b79-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61b79-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61b79-132">INPUTS</span></span>

## <span data-ttu-id="61b79-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61b79-133">OUTPUTS</span></span>

### <span data-ttu-id="61b79-134">ciąg</span><span class="sxs-lookup"><span data-stu-id="61b79-134">string</span></span>
<span data-ttu-id="61b79-135">Jeśli PassThru jest określony, zwraca zaktualizowany właściciel.</span><span class="sxs-lookup"><span data-stu-id="61b79-135">If PassThru is specified, returns the updated owner.</span></span>

## <span data-ttu-id="61b79-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61b79-136">NOTES</span></span>

## <span data-ttu-id="61b79-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61b79-137">RELATED LINKS</span></span>

[<span data-ttu-id="61b79-138">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="61b79-138">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


