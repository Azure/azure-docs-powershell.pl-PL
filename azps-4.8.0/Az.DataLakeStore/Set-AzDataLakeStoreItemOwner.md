---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: fc7c0e7ff8ef86b4a33f93e6b1286bb6e0baa00d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221791"
---
# <span data-ttu-id="6aade-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="6aade-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="6aade-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6aade-102">SYNOPSIS</span></span>
<span data-ttu-id="6aade-103">Modyfikuje właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6aade-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6aade-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6aade-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aade-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6aade-105">DESCRIPTION</span></span>
<span data-ttu-id="6aade-106">Polecenie cmdlet **Set-AzDataLakeStoreItemOwner** modyfikuje właściciela pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6aade-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6aade-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6aade-107">EXAMPLES</span></span>

### <span data-ttu-id="6aade-108">Przykład 1. Ustawianie właściciela elementu</span><span class="sxs-lookup"><span data-stu-id="6aade-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="6aade-109">To polecenie ustawia właściciela katalogu głównego, aby Patti pełen.</span><span class="sxs-lookup"><span data-stu-id="6aade-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="6aade-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6aade-110">PARAMETERS</span></span>

### <span data-ttu-id="6aade-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="6aade-111">-Account</span></span>
<span data-ttu-id="6aade-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6aade-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6aade-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aade-113">-DefaultProfile</span></span>
<span data-ttu-id="6aade-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6aade-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aade-115">-ID</span><span class="sxs-lookup"><span data-stu-id="6aade-115">-Id</span></span>
<span data-ttu-id="6aade-116">Określa identyfikator obiektu użytkownika, grupy lub podmiotu zabezpieczeń usługi AzureActive, który ma być używany jako właściciel.</span><span class="sxs-lookup"><span data-stu-id="6aade-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="6aade-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6aade-117">-PassThru</span></span>
<span data-ttu-id="6aade-118">Wskazuje, że zaktualizowany właściciel powinien zostać zwrócony.</span><span class="sxs-lookup"><span data-stu-id="6aade-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="6aade-119">-Path</span><span class="sxs-lookup"><span data-stu-id="6aade-119">-Path</span></span>
<span data-ttu-id="6aade-120">Określa ścieżkę elementu, który należy zmodyfikować, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="6aade-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6aade-121">-Type</span><span class="sxs-lookup"><span data-stu-id="6aade-121">-Type</span></span>
<span data-ttu-id="6aade-122">Określa typ właściciela do ustawienia.</span><span class="sxs-lookup"><span data-stu-id="6aade-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="6aade-123">Dopuszczalne wartości tego parametru to: użytkownik i Grupa.</span><span class="sxs-lookup"><span data-stu-id="6aade-123">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="6aade-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6aade-124">-Confirm</span></span>
<span data-ttu-id="6aade-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aade-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aade-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aade-126">-WhatIf</span></span>
<span data-ttu-id="6aade-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aade-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aade-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6aade-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aade-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aade-129">CommonParameters</span></span>
<span data-ttu-id="6aade-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aade-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aade-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aade-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aade-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6aade-132">INPUTS</span></span>

### <span data-ttu-id="6aade-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6aade-133">System.String</span></span>

### <span data-ttu-id="6aade-134">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6aade-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6aade-135">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="6aade-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="6aade-136">System. GUID</span><span class="sxs-lookup"><span data-stu-id="6aade-136">System.Guid</span></span>

### <span data-ttu-id="6aade-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6aade-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6aade-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6aade-138">OUTPUTS</span></span>

### <span data-ttu-id="6aade-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6aade-139">System.String</span></span>

## <span data-ttu-id="6aade-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6aade-140">NOTES</span></span>

## <span data-ttu-id="6aade-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6aade-141">RELATED LINKS</span></span>

[<span data-ttu-id="6aade-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="6aade-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


